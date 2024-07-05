<?php
?>
<head>
	<meta charset="UTF-8">
	<meta name="viewport" content="width=device-width, initial-scale=1.0">
	<title>Rotating Banner</title>
	<style>
		.banner-container {
			position: relative;
			max-width: 100%;
			margin: 0 auto;
			overflow: hidden; /* Impede que os slides ultrapassem a largura do container */
		}

		.banner-slides {
			display: flex;
			transition: transform 0.5s ease-in-out; /* Adiciona uma transição suave ao transform */
		}

		.slide {
			flex: 0 0 100%;
			padding: 20px;
			text-align: center;
		}

		button.ban_button {
			position: absolute;
			top: 50%;
			transform: translateY(-50%);
			padding: 10px 20px;
			background-color: #572183;
			color: #fff;
			border: none;
			cursor: pointer;
		}

		#prev {
			left: 0;
		}

		#next {
			right: 0;
		}

		.ban_img{
			height: 70%;
			width: 70%;
		}
		
	</style>
	<script>
		let slideIndex = 0;

		function showSlides() {
		  const slides = document.querySelectorAll('.slide');
		  if (slideIndex >= slides.length){
			  slideIndex = 0;
		  } else if (slideIndex < 0){
			  slideIndex = slides.length-1;
		  }
		  const slideWidth = slides[0].clientWidth; // Obtém a largura de um slide
		  const offset = -slideIndex * slideWidth; // Calcula o deslocamento

		  document.querySelector('.banner-slides').style.transform = `translateX(${offset}px)`;
		}

		function nextSlide() {
		  slideIndex++;
		  showSlides();
		}

		function prevSlide() {
		  slideIndex--;
		  showSlides();
		}

		document.addEventListener('DOMContentLoaded', showSlides);

	</script>
</head>
<body>
	<div class="banner-container">
		<div class="banner-slides">
			<?$href = explode(",", "".$img);?>
			<div class="slide"><img class="ban_img" src="<?echo "".$href[0]?>"></div>
			<?
			for ($x = 0; $x < $n; $x++) { 
				if ($x > 0) {
					echo "<div class='slide'><img class='ban_img' src=".$href[$x]."></img></div>";
				}
			}
			?>
		</div>
		<button class="ban_button" id="prev" onclick="prevSlide()"><i class="fa fa-angle-left"></i></button>
		<button class="ban_button" id="next" onclick="nextSlide()"><i class="fa fa-angle-right"></i></button>
	</div>
</body>
?>
