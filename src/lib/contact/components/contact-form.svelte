<script lang="ts">
   import {
       Button,
       EmailField,
       InputField,
       PhoneField,
       showToast,
       TextareaField
   } from '@cloudparker/moldex.js';

   let name: string = $state('');
   let email: string = $state('');
   let phone: string = $state('');
   let message: string = $state('');

	async function handleSubmit(e:any) {
    e.preventDefault();

    // Trim inputs
    name = (name || '').trim();
    email = (email || '').trim();
    phone = (phone || '').trim();
    message = (message || '').trim();

    // Validate required fields
    if (name && message && (email || phone)) {
      try {
        const response = await fetch('https://formspree.io/f/xldjdjyw', {
          method: 'POST',
          headers: {
            'Content-Type': 'application/json'
          },
          body: JSON.stringify({
            name,
            email,
            phone,
            message
          })
        });

        if (response.ok) {
          showToast({ msg: 'Message sent successfully!' });

          // Reset form fields
          name = '';
          email = '';
          phone = '';
          message = '';
        } else {
          showToast({ msg: 'Failed to send message. Please try again later.' });
        }
      } catch (error) {
        console.error('Error submitting form:', error);
        showToast({ msg: 'Something went wrong!' });
      }
    } else {
      showToast({ msg: 'Missing Required Fields!' });
    }
  }
</script>

<div class="relative mx-auto my-16 rounded-lg p-0.5 px-4 shadow-xl md:my-32 md:px-16 lg:px-32">
	<div class="bg-base-900 relative z-10 rounded-lg p-6 md:p-8">
		<h2 class="mb-4 text-center text-2xl font-bold text-white md:text-3xl">Get in Touch</h2>
		<p class="text-base-400 mb-8 text-center">
			We'd love to hear from you. Reach out to us for any inquiries or feedback.
		</p>
		<div class="grid grid-cols-1 gap-12 md:grid-cols-2">
			<div>
				<form class="space-y-5 " onsubmit={handleSubmit}>
					<div>
						<InputField placeholder="Name"  bind:value={name} size="lg" />
					</div>

					<div>
						<EmailField placeholder="Email Address" bind:value={email} size="lg" />
					</div>

					<!-- <div>
						<PhoneField placeholder="Phone" bind:value={phone} size="lg" />
					</div>

					<div>
						<TextareaField placeholder="Message" bind:value={message} size="lg" />
					</div> -->

					<div>
						<Button label="Send Message" type="submit" appearance="border-primary" className="w-full" />
					</div>
				</form>
			</div>
			<div>
				<div class="bg-base-800 h-full w-full rounded-lg p-6 md:p-8">
					<h3 class="mb-4 text-lg font-bold text-white md:text-xl">Contact Information</h3>
					<p class="text-base-400 mb-4">
						Have questions? We're here to help. Reach out to us for any inquiries or feedback.
					</p>
					<p class="text-base-400 mb-4">
						Email: <a href="mailto:support@hellocall.ai" class="text-primary-500"
							>support@hellocall.ai</a
						>
					</p>
					<p class="text-base-400 mb-4">
						Phone: <a href="tel:+91-8050770132" class="text-primary-500">+91-8050770132</a>
					</p>
				</div>
			</div>
		</div>
	</div>
</div>


