<script>
export default {
	data() {
		return {
			footerLinks: [
				{
					title: "DC Comics",
					links: ["Characters", "Comics", "Movies", "Games", "Videos", "News"]
				},
				{
					title: "Shop",
					links: ["Shop DC", "Shop DC Collectibles"]
				},
				{
					title: "DC",
					links: ["Terms of use", "Privacy policy", "Ad Choices", "Advertising", "Jobs", "Subscriptions", "Talent Workshops", "CPSC Certificates", "Ratings", "Shop Helop", "Contact Us"]
				},
				{
					title: "Sites",
					links: ["DC", "MAD Magazine", "DC Kids", "DC Universe", "DC Power Visa"]
				}
			]
		}
	}
}
</script>

<template>
	<footer>
		<div class="top-footer">
			<div class="container d-flex  justify-content-between">
				<div class="flex-left-side d-flex gap-4">
					<div class="footer-links" v-for="linkGroup in footerLinks">
						<h4 class="footer-link-title">{{ linkGroup.title.toUpperCase() }}</h4>
						<ul>
							<li class="footer-link-list" v-for="link in linkGroup.links">
								<a href="#">{{ link }}</a>
							</li>
						</ul>
					</div>
				</div>
				<div class="footer-logo">
					<img src="../assets/img/dc-logo-bg.png" alt="">
				</div>
			</div>
		</div>

		<div class="bottom-footer">
			<div class="container d-flex justify-content-between align-items-center">
				<div class="signup-btn">
					SIGN-UP NOW!
				</div>
				<div class="social-media-links d-flex">
					<div class="follow-us-link">
						<a href="#">FOLLOW US</a>
					</div>
					<div class="social-media-icon">
						<img src="../assets/img/footer-facebook.png" alt="">
					</div>
					<div class="social-media-icon">
						<img src="../assets/img/footer-periscope.png" alt="">
					</div>
					<div class="social-media-icon">
						<img src="../assets/img/footer-pinterest.png" alt="">
					</div>
					<div class="social-media-icon">
						<img src="../assets/img/footer-twitter.png" alt="">
					</div>
					<div class="social-media-icon">
						<img src="../assets/img/footer-youtube.png" alt="">
					</div>
				</div>
			</div>

		</div>
	</footer>
</template>

<style lang="scss" scoped>
.top-footer {
	display: flex;
	background-image: url(../assets/img/footer-bg.jpg);

	.flex-left-side {}


	.footer-logo {
		height: 400px;
		overflow: hidden;

		img {
			margin-top: -40px;
			width: 100%;
			object-fit: cover;
			object-position: right;
		}
	}

	.footer-links {
		padding-top: 2rem;

		h4 {
			padding-right: 2rem;
			color: white;
			font-weight: 700;
		}

		a {
			color: grey;
			text-decoration: none;
		}

		ul {
			padding-left: 0;
		}
	}
}

.bottom-footer {
	padding: 20px 0;
	background-color: #303030;

	.signup-btn {
		display: inline-block;
		color: white;
		padding: 0.8rem 1rem;
		border: 2px solid #0282F9;
	}

	.follow-us-link a{
		padding-right: 1rem;
		font-size: 1.4rem;
		color:#0282F9 ;
		text-decoration: none;
	}

	.social-media-icon{
		padding-right: 1rem;
	}
}
</style>
