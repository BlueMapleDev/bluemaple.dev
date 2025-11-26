<section class="grid place-items-center" id="contact">
	<!-- <h2 class="text-5xl text-center font-bold my-4">Contact Me</h2> -->
	<form method="POST" class="sm:w-5/12 space-y-4">
		<div class="grid grid-cols-1">
			<label class="text-xl" for="name">Name</label>
			<input type="text" name="name" required class="text-black pl-2" />
		</div>
		<div class="grid grid-cols-1">
			<label class="text-xl" for="email">Email</label>
			<input type="email" name="email" required class="text-black pl-2" />
		</div>
		<div class="grid grid-cols-1">
			<label class="text-xl" for="message">Message</label>
			<textarea name="message" cols="30" rows="10" required class="text-black p-2"></textarea>
		</div>
		<div class="grid place-content-center">
			<button type="submit" class="border border-white bg-green-700 pl-2 text-lg">Send email</button>
		</div>
	</form>
</section>
