<script lang="ts">
	import { Button, EmailField, InputField, showToast, TextareaField } from '@cloudparker/moldex.js';

	let name: string = $state('');
	let email: string = $state('');
	let phone: string = $state('');
	let message: string = $state('');

	async function handleSubmit(e: Event) {
		e.preventDefault();

		// Trim inputs
		name = (name || '').trim();
		email = (email || '').trim();
		phone = (phone || '').trim();
		message = (message || '').trim();

		// Validate required fields
		if (name && email) {
			try {
				const response = await fetch('https://formspree.io/f/xzzvzgyd', {
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
			showToast({ msg: 'Name and Email are required!' });
		}
	}
</script>

<div class="relative mx-auto my-16 rounded-lg p-0.5 px-4 shadow-xl md:my-32 md:px-16">
	<div class="relative z-10 rounded-lg bg-base-900 p-6 md:p-8">
		<h2 class="mb-4 text-center text-2xl font-bold text-white md:text-3xl">Get in Touch</h2>
		<p class="mb-8 text-center text-base-400">
			We'd love to hear from you. Reach out to us for any inquiries or feedback.
		</p>
		<div class="grid grid-cols-1 gap-12 md:grid-cols-2">
			<div>
				<form class="space-y-5" onsubmit={handleSubmit}>
					<div>
						<InputField
							placeholder="Your Name"
							name="name"
							type="text"
							bind:value={name}
							size="lg"
							required
						/>
					</div>

					<div>
						<EmailField
							placeholder="Your Email Address"
							name="email"
							type="email"
							bind:value={email}
							size="lg"
							required
						/>
					</div>

					<div>
						<input
							type="tel"
							placeholder="Your Phone Number"
							name="phone"
							bind:value={phone}
							class="w-full rounded-lg border border-gray-600 bg-base-700 px-4 py-3 text-base-200 focus:border-primary-600 focus:bg-base-800 focus:outline-none"
						/>
					</div>

					<div>
						<textarea
							name="message"
							placeholder="Your Message"
							bind:value={message}
							rows="5"
							class="w-full resize-none rounded-lg border border-gray-700 bg-base-700 px-4 py-3 text-base-200 focus:border-primary-600 focus:bg-base-800 focus:outline-none"
						></textarea>
					</div>

					<div>
						<Button
							label="Send Message"
							type="submit"
							appearance="border-primary"
							className="w-full"
							disabled={!name || !email}
						>
							Send Message
						</Button>
					</div>
				</form>
			</div>
			<div>
				<div class="h-full w-full rounded-lg bg-base-800 p-6 md:p-8">
					<h3 class="mb-4 text-lg font-bold text-white md:text-xl">Contact Information</h3>
					<p class="mb-4 text-base-400">
						Have questions? We're here to help. Reach out to us for any inquiries or feedback.
					</p>
					<div class="space-y-4">
						<div class="flex items-start space-x-3">
							<!-- <svg class="mt-1 h-5 w-5 flex-shrink-0 text-primary-500" fill="currentColor" viewBox="0 0 20 20">
								<path fill-rule="evenodd" d="M2.166 4.999A11.954 11.954 0 0010 1.944 11.954 11.954 0 0017.834 5c.11.65.166 1.32.166 2.001 0 5.225-3.34 9.67-8 11.317C5.34 16.67 2 12.225 2 7c0-.682.057-1.35.166-2.001zm11.541 0a9.501 9.501 0 00-9.9 8.180.366.366 0 00.344.28h3.453a2 2 0 011.508-.827l.428-1.828a2 2 0 012.286-1.356l.151.755a4 4 0 005.861 1.314l.846-1.79a.5.5 0 00-.49-.595l-1.914-.371a6 6 0 00-5.391-3.402Z" clip-rule="evenodd" />
							</svg> -->
							<div>
								<p class="text-base-400">Email</p>
								<p class="text-sm">
									<a
										href="mailto:lampvoltoffice@gmail.com"
										class="text-primary-500 transition-colors hover:text-primary-400"
									>
										lampvoltoffice@gmail.com
									</a>
								</p>
							</div>
						</div>

						<div class="flex items-start space-x-3">
							<!-- <svg class="mt-1 h-5 w-5 flex-shrink-0 text-primary-500" fill="currentColor" viewBox="0 0 20 20">
								<path d="M2 3a1 1 0 011-1h2.153a1 1 0 01.986.836l.74 4.435a1 1 0 01-.54 1.06l-1.548.773a11.037 11.037 0 006.105 6.105l.774-1.548a1 1 0 011.059-.54l4.435.74a1 1 0 01.836.986V17a1 1 0 01-1 1h-2C7.82 18 2 12.18 2 5V3z" />
							</svg> -->
							<div>
								<p class="text-base-400">Phone</p>
								<p class="text-sm">
									<a
										href="tel:+916370888479"
										class="text-primary-500 transition-colors hover:text-primary-400"
									>
										+91 63708 88479
									</a>
								</p>
							</div>
						</div>
					</div>
				</div>
			</div>
		</div>
	</div>
</div>
