<div class="container">
	<img
		src="https://cdn4.iconfinder.com/data/icons/scripting-and-programming-languages/512/Python_logo-512.png"
		alt="py"
		width="40px"
		height="40px"
	/>
	<nav>Pyplan</nav>
</div>
<div class="container">
	<p>why pyplan?</p>
	<p>platform</p>
	<p>solutions</p>
	<p>cases</p>
	<p>partners</p>
</div>
<div class="container">
	<button>Get in touch</button>
</div>

<style>
	.container {
		font-family: 'Poppins', sans-serif;
		display: flex; /* Enables Flexbox */
		align-items: center;
	}
	nav {
		font-size: var(--font-size-h3);
		font-weight: var(font-weight-regular);
	}

	img,
	nav {
		margin-right: 10px; /* Adds spacing between the image and the text */
	}

	p {
		font-size: clamp(var(--font-size-small));
		font-weight: var(--font-weight-regular);
		margin: 0 7px 0 7px;
	}

	p:hover {
		cursor: pointer;
	}

	button {
		/* aligning */
		display: flex;
		justify-content: center;
		align-items: center;

		/* font */
		font-size: var(--font-size-button);
		font-weight: var(--font-weight-button);

		/* size */
		width: 181px;
		height: 38px;

		/* border */
		border-radius: 4px;
		border: 2px solid black;
		box-shadow:
			0px 8px 16px 0px rgba(96, 97, 112, 0.16),
			0px 2px 4px 0px rgba(40, 41, 61, 0.04);

		transition: background-color 0.4s;
	}
	button:hover {
		cursor: pointer;
		background-color: black;
		color: white;
	}
</style>
