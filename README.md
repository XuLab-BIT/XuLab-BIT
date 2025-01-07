# Welcome to XuLab！

![Lab Members](http://1304199935.vod-qcloud.com/ba849d0evodcq1304199935/3119f5e81253642700552398894/w4xRqHm2A7cA.png) 

---

## Fan Xu

**Principal Investigator**

xufan@bit.edu.cn

Lab Website：www.XuLab.cc

### Profile

Fan Xu is a Professor at the Advanced Research Institute of Multidisciplinary Sciences, Beijing Institute of Technology (BIT). He earned his B.S. in Computer Science and Technology from BIT in 2011 and his Ph.D. in Computer Science and Technology from the University of Chinese Academy of Sciences in 2017. Before joining BIT, Dr. Xu worked as a Postdoctoral Fellow and Senior Research Associate with Fang Huang in the Weldon School of Biomedical Engineering at Purdue University.

### Research Interests

Dr. Xu's research focuses on the development and application of super-resolution microscopy techniques, particularly in the areas of 3D super-resolution imaging and single molecule localization analysis. He combines innovative imaging instruments with physical models or data-driven approaches to explore cellular and tissue structures and dynamics that are below the diffraction limit of light and thus inaccessible to conventional microscopy.



<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Image Carousel</title>
    <style>
        body {
            margin: 0;
            font-family: Arial, sans-serif;
            background-color: black;
            color: white;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            overflow: hidden;
        }
<div class="carousel">
    <div class="carousel-images">
        <img src="http://1304199935.vod-qcloud.com/ba849d0evodcq1304199935/a3e30fba1253642700540096726/K1UDUbLm3LoA.png" alt="Image 1">
        <img src="http://1304199935.vod-qcloud.com/ba849d0evodcq1304199935/7a21b57d1253642700539652534/zBIfSagx4doA.png" alt="Image 2">
        <img src="http://1304199935.vod-qcloud.com/ba849d0evodcq1304199935/a820c1b71253642700540236466/rxgKiotmLoYA.png" alt="Image 3">
    </div>
    <div class="carousel-controls">
        <button id="prevBtn">&#8249;</button>
        <button id="nextBtn">&#8250;</button>
    </div>
</div>


<style>
.carousel {
    position: relative;
    width: 80%;
    max-width: 1000px;
    height: 500px;
    overflow: hidden;
    border-radius: 10px;
}
.carousel-images {
    display: flex;
    transition: transform 0.5s ease-in-out;
}
.carousel-images img {
    width: 100%;
    height: 100%;
    object-fit: cover;
}
.carousel-controls {
    position: absolute;
    top: 50%;
    width: 100%;
    display: flex;
    justify-content: space-between;
    transform: translateY(-50%);
    z-index: 10;
}
.carousel-controls button {
    background-color: rgba(0, 0, 0, 0.5);
    border: none;
    color: white;
    font-size: 2rem;
    cursor: pointer;
    padding: 10px;
    border-radius: 50%;
}
.carousel-controls button:hover {
    background-color: rgba(255, 255, 255, 0.5);
}
</style>

<script>
const carouselImages = document.querySelector('.carousel-images');
const images = document.querySelectorAll('.carousel-images img');
const prevBtn = document.getElementById('prevBtn');
const nextBtn = document.getElementById('nextBtn');

let index = 0;

function updateCarousel() {
    const width = images[index].clientWidth;
    carouselImages.style.transform = `translateX(${-index * width}px)`;
}

prevBtn.addEventListener('click', () => {
    index = (index - 1 + images.length) % images.length;
    updateCarousel();
});

nextBtn.addEventListener('click', () => {
    index = (index + 1) % images.length;
    updateCarousel();
});

window.addEventListener('resize', updateCarousel);
</script>
