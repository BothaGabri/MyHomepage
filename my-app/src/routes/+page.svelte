<script>
	
</script>


<main>

	<!-- Contact Section -->
	<div class="contact-section">
		<div class="contact-card">
			<h1><u>Gabri:</u></h1>
			<p>
				<strong><u>Whatsapp:</u></strong>
				<a href="tel:0660754176">0660754176</a>
			</p>
			<p>
				<strong><u>Email:</u></strong>
				<a href="mailto:bothagabri@gmail.com">bothagabri@gmail.com</a>
			</p>
		</div>
	</div>
</main>

<!-- Bottom Border -->
<div class="border bottom"></div>

<style>
	:global(body) {
		margin: 0;
		padding: 0;
		font-family: Arial, sans-serif; /* Keep basic font like flyer */
		background-color: #f8f8f8; /* Very light grey, subtle contrast */
	}

	main {
		display: flex;
		flex-direction: column;
		align-items: center;
		padding: 40px 20px;
		max-width: 900px;
		margin: 0 auto;
	}

	/* Jagged Borders */
	.border {
		width: 100%;
		height: 40px;
		background-image: linear-gradient(
			45deg,
			black 25%,
			transparent 25%,
			transparent 75%,
			black 75%
		);
		background-size: 20px 20px;
		background-position: 0 0, 10px 10px;
	}
	.border.bottom {
		transform: rotate(180deg);
	}

	
	/* Contact Section */
	.contact-section {
		width: 100%;
		display: flex;
		justify-content: center;
		padding: 50px 0;
	}
	.contact-card {
		background-color: #4caf50; /* Flyer Green */
		border: 1.5px solid #333;
		border-radius: 30px;
		padding: 30px 40px;
		text-align: center;
		box-shadow: 0 4px 10px rgba(0, 0, 0, 0.2);
		width: 80%;
		max-width: 600px;
	}
	.contact-card h1,
	.contact-card p,
	.contact-card a {
		font-family: Arial, sans-serif;
		color: #333;
	}
	.contact-card h1 {
		margin-top: 0;
		font-size: 2.5rem;
	}
	.contact-card p {
		font-size: 1.4rem;
		margin: 15px 0;
	}
	.contact-card a {
		text-decoration: none;
		color: inherit;
		font-weight: bold;
	}
	.contact-card a:hover {
		color: white;
	}

	/* Mobile Responsiveness */
	@media (max-width: 768px) {
		.contact-card h1 {
			font-size: 2rem;
		}
		.contact-card p {
			font-size: 1.1rem;
		}
	}
</style>