<!doctype html>
<html lang="es"><head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Galería de Imágenes</title>
  <script src="https://cdn.tailwindcss.com/3.4.17"></script>
  <link href="https://fonts.googleapis.com/css2?family=DM+Sans:wght@400;500;700&amp;family=Playfair+Display:wght@700&amp;display=swap" rel="stylesheet">
  <style>
    body { font-family: 'DM Sans', sans-serif; }
    .thumb-active { ring: 2px; box-shadow: 0 0 0 3px rgba(255,255,255,0.8); }
  </style>
  <script src="https://cdn.jsdelivr.net/npm/lucide@0.263.0/dist/umd/lucide.min.js" type="text/javascript"></script>
  <script src="/_sdk/data_sdk.js" type="text/javascript"></script>
  <script src="/_sdk/resizing_sdk.js" type="text/javascript"></script>
 </head>
 <body data-template-id="__page-root" class="min-h-screen w-full" style="background: rgb(15, 15, 15);">
  <main class="max-w-5xl mx-auto px-4 py-12">
   <header class="text-center mb-8">
    <h1 data-template-id="gallery-title" class="canva-text" style="font-family: &quot;Playfair Display&quot;, serif; color: rgb(245, 245, 244); font-weight: 700; font-style: normal; font-size: 32px;">Galería de Imágenes</h1>
    <p data-template-id="gallery-subtitle" class="canva-text mt-3" style="color: rgb(168, 162, 158); font-weight: 400; font-style: normal; font-size: 18px;">Selecciona una imagen para verla en grande</p>
   </header><!-- Featured image -->
   <div class="w-full rounded-xl overflow-hidden shadow-2xl mb-6"><img id="featured" class="w-full object-cover" style="max-height:500px;" loading="lazy">
   </div><!-- Thumbnails -->
   <div class="grid grid-cols-3 sm:grid-cols-6 gap-3"><button class="thumb rounded-lg overflow-hidden border-2 border-transparent focus:outline-none" onclick="selectImage(0)"> <img data-template-id="img-1" class="canva-image w-full h-20 sm:h-24 object-cover" loading="lazy" src="https://images.pexels.com/photos/1032650/pexels-photo-1032650.jpeg?auto=compress&amp;cs=tinysrgb&amp;w=1280" alt="Serene sunset over Ludington Beach with vibrant colors and tranquil waves"> </button> <button class="thumb rounded-lg overflow-hidden border-2 border-transparent focus:outline-none" onclick="selectImage(1)"> <img data-template-id="img-2" class="canva-image w-full h-20 sm:h-24 object-cover" loading="lazy" src="https://images.pexels.com/photos/1671324/pexels-photo-1671324.jpeg?auto=compress&amp;cs=tinysrgb&amp;w=1280" alt="Mysterious dark foggy forest pathway surrounded by towering trees"> </button> <button class="thumb rounded-lg overflow-hidden border-2 border-transparent focus:outline-none" onclick="selectImage(2)"> <img data-template-id="img-3" class="canva-image w-full h-20 sm:h-24 object-cover" loading="lazy" src="https://images.pexels.com/photos/1519088/pexels-photo-1519088.jpeg?auto=compress&amp;cs=tinysrgb&amp;w=1280" alt="Stunning night view of Toronto skyline reflecting on water with CN Tower"> </button> <button class="thumb rounded-lg overflow-hidden border-2 border-transparent focus:outline-none" onclick="selectImage(3)"> <img data-template-id="img-4" class="canva-image w-full h-20 sm:h-24 object-cover" loading="lazy" src="https://images.pexels.com/photos/36181722/pexels-photo-36181722.jpeg?auto=compress&amp;cs=tinysrgb&amp;w=1280" alt="Dramatic golden sand dunes illuminated by warm sunset glow"> </button> <button class="thumb rounded-lg overflow-hidden border-2 border-transparent focus:outline-none" onclick="selectImage(4)"> <img data-template-id="img-5" class="canva-image w-full h-20 sm:h-24 object-cover" loading="lazy" src="https://images.pexels.com/photos/2743287/pexels-photo-2743287.jpeg?auto=compress&amp;cs=tinysrgb&amp;w=1280" alt="Majestic waterfall cascading through lush jungle foliage in India"> </button> <button class="thumb rounded-lg overflow-hidden border-2 border-transparent focus:outline-none" onclick="selectImage(5)"> <img data-template-id="img-6" class="canva-image w-full h-20 sm:h-24 object-cover" loading="lazy" src="https://images.pexels.com/photos/29453841/pexels-photo-29453841.jpeg?auto=compress&amp;cs=tinysrgb&amp;w=1280" alt="Sunlit autumn forest path with colorful leaves in Warsaw, Poland"> </button>
   </div>
  </main>
  <script src="/_sdk/editing_sdk.js"></script>
  <script>
    const featured = document.getElementById('featured');
    const thumbs = document.querySelectorAll('.thumb');

    function selectImage(index) {
      const img = thumbs[index].querySelector('img');
      if (img.src) {
        featured.src = img.src;
        featured.alt = img.alt || '';
      }
      thumbs.forEach((t, i) => {
        t.classList.toggle('border-white', i === index);
        t.classList.toggle('border-transparent', i !== index);
        t.classList.toggle('opacity-60', i !== index);
        t.classList.toggle('opacity-100', i === index);
      });
    }

    // Wait for SDK to apply images then set first as featured
    setTimeout(() => selectImage(0), 300);
  </script>
 <script>(function(){function c(){var b=a.contentDocument||a.contentWindow.document;if(b){var d=b.createElement('script');d.innerHTML="window.__CF$cv$params={r:'9fafbd3037edda28',t:'MTc3ODY1NTEzMi4wMDAwMDA='};var a=document.createElement('script');a.nonce='';a.src='/cdn-cgi/challenge-platform/scripts/jsd/main.js';document.getElementsByTagName('head')[0].appendChild(a);";b.getElementsByTagName('head')[0].appendChild(d)}}if(document.body){var a=document.createElement('iframe');a.height=1;a.width=1;a.style.position='absolute';a.style.top=0;a.style.left=0;a.style.border='none';a.style.visibility='hidden';document.body.appendChild(a);if('loading'!==document.readyState)c();else if(window.addEventListener)document.addEventListener('DOMContentLoaded',c);else{var e=document.onreadystatechange||function(){};document.onreadystatechange=function(b){e(b);'loading'!==document.readyState&&(document.onreadystatechange=e,c())}}}})();</script>
</body></html>
