<!DOCTYPE html>
<html lang="th" class="scroll-smooth">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Rogafry - Art & Fashion Café</title>
    <!-- Tailwind CSS CDN -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- Google Font: Prompt & Playfair Display -->
    <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:ital,wght@0,400;0,700;1,400&family=Prompt:wght@300;400;500;600;700&display=swap" rel="stylesheet">
    <!-- FontAwesome Icons -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    fontFamily: {
                        sans: ['Prompt', 'sans-serif'],
                        serif: ['Playfair Display', 'serif']
                    },
                    colors: {
                        victorian: {
                            bg: '#1a120b',
                            card: '#2c221e',
                            gold: '#d4af37',
                            accent: '#8b0000',
                            text: '#f3e5ab'
                        },
                        roman: {
                            bg: '#fbf9f1',
                            card: '#f4ede2',
                            gold: '#b8860b',
                            accent: '#2b4c7e',
                            text: '#2c221e'
                        },
                        vibrant: {
                            bg: '#0f0c1b',
                            card: '#1e1b2e',
                            gold: '#ff3366',
                            accent: '#00f0ff',
                            text: '#ffffff'
                        }
                    }
                }
            }
        }
    </script>
    <style>
        .theme-victorian {
            --bg-color: #1a120b;
            --card-bg: #2c221e;
            --gold-color: #d4af37;
            --accent-color: #8b0000;
            --text-color: #f3e5ab;
            --border-color: #d4af37;
        }
        .theme-roman {
            --bg-color: #fcfbfa;
            --card-bg: #f4ede2;
            --gold-color: #b8860b;
            --accent-color: #2b4c7e;
            --text-color: #2c221e;
            --border-color: #b8860b;
        }
        .theme-vibrant {
            --bg-color: #0d0b18;
            --card-bg: #18152e;
            --gold-color: #ff3366;
            --accent-color: #00f0ff;
            --text-color: #ffffff;
            --border-color: #ff3366;
        }
        body {
            background-color: var(--bg-color, #1a120b);
            color: var(--text-color, #f3e5ab);
            transition: background-color 0.5s ease, color 0.5s ease;
        }
    </style>
</head>
<body class="theme-victorian" id="bodyTheme">

    <!-- Navbar -->
    <header class="sticky top-0 z-50 backdrop-blur-md bg-opacity-80 border-b border-amber-600/30 transition-colors duration-500" style="background-color: var(--card-bg);">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 h-20 flex items-center justify-between">
            <a href="#" class="flex items-center space-x-3">
                <i class="fa-solid fa-palette text-2xl" style="color: var(--gold-color);"></i>
                <span class="text-2xl font-serif font-bold tracking-wider" style="color: var(--gold-color);">ROGAFRY</span>
            </a>
            
            <nav class="hidden md:flex items-center space-x-8 font-medium">
                <a href="#about" class="hover:opacity-75 transition">เกี่ยวกับเรา</a>
                <a href="#theme-section" class="hover:opacity-75 transition">ธีมร้าน</a>
                <a href="#gallery" class="hover:opacity-75 transition">แกลเลอรี & ประมูล</a>
                <a href="#workshop" class="hover:opacity-75 transition">เวิร์กช็อป</a>
                <a href="#menu" class="hover:opacity-75 transition">คาเฟ่ & แฟชั่น</a>
                <a href="#art-therapy" class="hover:opacity-75 transition">มุมฮีลใจ</a>
            </nav>

            <div class="flex items-center space-x-4">
                <!-- Theme Switcher -->
                <select id="themeSelector" onchange="changeTheme(this.value)" class="bg-transparent border px-3 py-1.5 rounded-lg text-sm focus:outline-none cursor-pointer" style="border-color: var(--gold-color); color: var(--text-color);">
                    <option value="victorian" class="bg-gray-900 text-white">👑 ธีมวิคตอเรีย (ม.ค.-ก.พ.)</option>
                    <option value="roman" class="bg-gray-900 text-white">🏛️ ธีมกรีซ-โรมัน (มี.ค.-เม.ย.)</option>
                    <option value="vibrant" class="bg-gray-900 text-white">🎨 ธีมโมเดิร์นสีสันสดใส</option>
                </select>
                <a href="#workshop" class="hidden sm:inline-block px-5 py-2 rounded-lg font-semibold shadow-lg transition transform hover:scale-105" style="background-color: var(--gold-color); color: #1a120b;">
                    จองคิวเวิร์กช็อป
                </a>
            </div>
        </div>
    </header>

    <!-- Hero Section -->
    <section class="relative py-24 md:py-32 overflow-hidden text-center px-4">
        <div class="max-w-4xl mx-auto space-y-6">
            <span class="inline-block px-4 py-1.5 rounded-full text-xs font-semibold uppercase tracking-widest border" style="border-color: var(--gold-color); color: var(--gold-color);">
                Art & Fashion Café • เปิดให้บริการ พฤหัสบดี - อังคาร (07.30 - 22.00)
            </span>
            <h1 class="text-4xl md:text-6xl font-serif font-bold leading-tight" style="color: var(--gold-color);">
                ROGAFRY (โรกาฟรี)
            </h1>
            <p class="text-lg md:text-xl font-light max-w-2xl mx-auto opacity-90">
                พื้นที่หลีกหนีความวุ่นวาย เติมเต็มจินตนาการ คลายเครียดจากงานและตำราเรียน ผ่านศิลปะ แฟชั่น และกลิ่นหอมกรุ่นของกาแฟ
            </p>
            <div class="flex flex-wrap justify-center gap-4 pt-4">
                <a href="#gallery" class="px-8 py-3 rounded-xl font-semibold border-2 transition hover:bg-opacity-10 hover:bg-white" style="border-color: var(--gold-color); color: var(--gold-color);">
                    ดูผลงานประมูล
                </a>
                <a href="#art-therapy" class="px-8 py-3 rounded-xl font-semibold shadow-xl transition transform hover:scale-105" style="background-color: var(--accent-color); color: #fff;">
                    🎨 ปลดปล่อยความเครียด (Art Therapy)
                </a>
            </div>
        </div>
    </section>

    <!-- About Section / Who & Why -->
    <section id="about" class="py-20 px-4" style="background-color: var(--card-bg);">
        <div class="max-w-6xl mx-auto grid md:grid-cols-2 gap-12 items-center">
            <div class="space-y-6">
                <h2 class="text-3xl font-serif font-bold" style="color: var(--gold-color);">คาเฟ่ที่มากกว่าร้านกาแฟ</h2>
                <p class="leading-relaxed opacity-90">
                    <strong>Rogafry</strong> เกิดขึ้นจากความตั้งใจสร้างพื้นที่ให้วัยรุ่น นักเรียน นักศึกษา และบุคคลทั่วไปที่มีความเครียดจากการเรียนหรือการทำงาน ได้เข้ามาผ่อนคลายอารมณ์ แสดงออกถึงตัวตนผ่านงานศิลปะ แฟชั่นร่วมสมัย และกิจกรรมเวิร์กช็อปสร้างสรรค์
                </p>
                <div class="grid grid-cols-2 gap-4 pt-2">
                    <div class="border p-4 rounded-xl" style="border-color: var(--gold-color);">
                        <i class="fa-solid fa-clock text-2xl mb-2" style="color: var(--gold-color);"></i>
                        <h4 class="font-bold">เวลาทำการ</h4>
                        <p class="text-sm opacity-80">พฤหัสบดี - อังคาร<br>07:30 - 22:00 น.</p>
                    </div>
                    <div class="border p-4 rounded-xl" style="border-color: var(--gold-color);">
                        <i class="fa-solid fa-heart-pulse text-2xl mb-2" style="color: var(--gold-color);"></i>
                        <h4 class="font-bold">Art Therapy</h4>
                        <p class="text-sm opacity-80">พื้นที่ฮีลใจ หัวร้อนง่ายมาทางนี้ ผ่อนคลายด้วยพู่กันและสีสัน</p>
                    </div>
                </div>
            </div>
            <div class="relative rounded-2xl overflow-hidden border-2 shadow-2xl h-80 md:h-96 flex items-center justify-center p-6 text-center" style="border-color: var(--gold-color);">
                <div class="space-y-4">
                    <i class="fa-solid fa-shirt text-6xl opacity-80" style="color: var(--gold-color);"></i>
                    <h3 class="text-2xl font-serif font-bold">Fashion & Art Integration</h3>
                    <p class="text-sm opacity-80">เสื้อผ้าแฟชั่นดีไซน์ฉูดฉาดผสมผสานยุคสมัยและวัสดุธรรมชาติ พร้อมจัดแสดงงานศิลปะหมุนเวียนตลอดปี</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Theme Rotation Section -->
    <section id="theme-section" class="py-20 px-4 max-w-6xl mx-auto">
        <div class="text-center space-y-4 mb-12">
            <h2 class="text-3xl font-serif font-bold" style="color: var(--gold-color);">การตกแต่งร้านตามช่วงเวลา (Theme Rotation)</h2>
            <p class="opacity-80 max-w-xl mx-auto">บรรยากาศร้านจะเปลี่ยนผ่านไปตามยุคสมัย เพื่อสร้างแรงบันดาลใจใหม่ๆ ทุกครั้งที่แวะมาเยี่ยมเยียน</p>
        </div>
        <div class="grid md:grid-cols-2 gap-8">
            <div class="p-8 rounded-2xl border transition hover:shadow-xl" style="background-color: var(--card-bg); border-color: var(--gold-color);">
                <span class="text-xs font-bold uppercase tracking-wider px-3 py-1 rounded-full border border-amber-500 text-amber-400">มกราคม - กุมภาพันธ์</span>
                <h3 class="text-2xl font-serif font-bold mt-4 mb-2">👑 ยุควิคตอเรีย (Victorian Era)</h3>
                <p class="opacity-90 leading-relaxed">สัมผัสความหรูหรา วิจิตรบรรจง ดีเทลลูกไม้ ความคลาสสิกของเครื่องเรือนไม้เข้ม และบรรยากาศอันลึกล้ำชวนฝัน</p>
            </div>
            <div class="p-8 rounded-2xl border transition hover:shadow-xl" style="background-color: var(--card-bg); border-color: var(--gold-color);">
                <span class="text-xs font-bold uppercase tracking-wider px-3 py-1 rounded-full border border-amber-500 text-amber-400">มีนาคม - เมษายน</span>
                <h3 class="text-2xl font-serif font-bold mt-4 mb-2">🏛️ กรีซ - โรมัน (Greco-Roman Era)</h3>
                <p class="opacity-90 leading-relaxed">ดื่มด่ำกับสถาปัตยกรรมเสาโรมัน ประติมากรรมหินอ่อน และความยิ่งใหญ่ทางประวัติศาสตร์ที่ผสานความร่วมสมัยอย่างลงตัว</p>
            </div>
        </div>
    </section>

    <!-- Art Therapy Digital Canvas (มุมฮีลใจ ปลดปล่อยความเครียด) -->
    <section id="art-therapy" class="py-20 px-4" style="background-color: var(--card-bg);">
        <div class="max-w-4xl mx-auto text-center space-y-6">
            <span class="px-4 py-1 rounded-full text-xs font-bold uppercase border" style="border-color: var(--gold-color); color: var(--gold-color);">Stress Relief Corner</span>
            <h2 class="text-3xl font-serif font-bold" style="color: var(--gold-color);">มุมฮีลใจ: ระบายสีสาดอารมณ์ดิจิทัล</h2>
            <p class="opacity-80">หัวร้อนจากงานหรือการเรียนใช่ไหม? ลองใช้เมาส์หรือนิ้วแตะลากสาดสีลงบนผืนผ้าใบจำลอง เพื่อปลดปล่อยความเครียดและความรู้สึกอัดอั้นออกมาเป็นศิลปะกัน!</p>
            
            <div class="flex justify-center items-center gap-4 py-2">
                <label class="text-sm font-semibold">เลือกสีพู่กัน:</label>
                <input type="color" id="brushColor" value="#ff3366" class="w-10 h-10 rounded cursor-pointer border-0 bg-transparent">
                <button onclick="clearCanvas()" class="px-4 py-2 rounded-lg text-sm font-semibold border transition hover:bg-white hover:text-black" style="border-color: var(--gold-color);">
                    ล้างผืนผ้าใบใหม่
                </button>
            </div>

            <div class="border-2 rounded-2xl overflow-hidden shadow-2xl bg-white cursor-crosshair relative">
                <canvas id="therapyCanvas" width="800" height="400" class="w-full h-[400px] touch-none"></canvas>
            </div>
            <p class="text-xs opacity-60">ลากเมาส์หรือใช้นิ้วมือวาดบนกล่องสี่เหลี่ยมด้านบนเพื่อระบายสีตามใจชอบ</p>
        </div>
    </section>

    <!-- Gallery & Live Art Auction (ประมูลผลงานศิลปะคอมมูนิตี้) -->
    <section id="gallery" class="py-20 px-4 max-w-6xl mx-auto">
        <div class="text-center space-y-4 mb-12">
            <span class="px-4 py-1 rounded-full text-xs font-bold uppercase border" style="border-color: var(--gold-color); color: var(--gold-color);">Community Auction</span>
            <h2 class="text-3xl font-serif font-bold" style="color: var(--gold-color);">ประมูลผลงานศิลปะชุมชน Rogafry</h2>
            <p class="opacity-80 max-w-xl mx-auto">ผลงานจากเวิร์กช็อปของสมาชิกและศิลปินรุ่นใหม่ รายได้ส่วนציสนับสนุนศิลปินและสมทบทุนการกุศล</p>
        </div>

        <div class="grid md:grid-cols-3 gap-8">
            <!-- Item 1 -->
            <div class="rounded-2xl border overflow-hidden shadow-xl flex flex-col justify-between" style="background-color: var(--card-bg); border-color: var(--gold-color);">
                <div class="h-56 bg-cover bg-center relative flex items-end p-4" style="background-image: url('https://images.unsplash.com/photo-1579783902614-a3fb3927b675?auto=format&fit=crop&q=80&w=600')">
                    <span class="bg-black/70 text-white text-xs px-3 py-1 rounded-full backdrop-blur-sm">ประมูลสดในเว็บ / FB Page</span>
                </div>
                <div class="p-6 space-y-4 flex-1 flex flex-col justify-between">
                    <div>
                        <h3 class="font-serif font-bold text-xl mb-1">"Victorian Dreamscape"</h3>
                        <p class="text-sm opacity-80">โดย คุณเหนือเมฆ (สมาชิกคอมมูนิตี้)</p>
                        <div class="mt-4 flex justify-between text-sm">
                            <span class="opacity-75">ราคาประมูลปัจจุบัน:</span>
                            <span class="font-bold text-amber-400" id="bidPrice1">1,450 บาท</span>
                        </div>
                    </div>
                    <div class="flex gap-2">
                        <input type="number" id="bidInput1" placeholder="เสนอราคาเพิ่ม" class="flex-1 bg-transparent border rounded-lg px-3 py-2 text-sm focus:outline-none" style="border-color: var(--gold-color);">
                        <button onclick="placeBid(1)" class="px-4 py-2 rounded-lg font-semibold text-sm transition" style="background-color: var(--gold-color); color: #1a120b;">เสนอราคา</button>
                    </div>
                </div>
            </div>

            <!-- Item 2 -->
            <div class="rounded-2xl border overflow-hidden shadow-xl flex flex-col justify-between" style="background-color: var(--card-bg); border-color: var(--gold-color);">
                <div class="h-56 bg-cover bg-center relative flex items-end p-4" style="background-image: url('https://images.unsplash.com/photo-1541963463532-d68292c34b19?auto=format&fit=crop&q=80&w=600')">
                    <span class="bg-black/70 text-white text-xs px-3 py-1 rounded-full backdrop-blur-sm">ประมูลสดในเว็บ / FB Page</span>
                </div>
                <div class="p-6 space-y-4 flex-1 flex flex-col justify-between">
                    <div>
                        <h3 class="font-serif font-bold text-xl mb-1">"Roman Marble Echo"</h3>
                        <p class="text-sm opacity-80">โดย คุณกานต์ (ศิลปินรับเชิญ)</p>
                        <div class="mt-4 flex justify-between text-sm">
                            <span class="opacity-75">ราคาประมูลปัจจุบัน:</span>
                            <span class="font-bold text-amber-400" id="bidPrice2">2,200 บาท</span>
                        </div>
                    </div>
                    <div class="flex gap-2">
                        <input type="number" id="bidInput2" placeholder="เสนอราคาเพิ่ม" class="flex-1 bg-transparent border rounded-lg px-3 py-2 text-sm focus:outline-none" style="border-color: var(--gold-color);">
                        <button onclick="placeBid(2)" class="px-4 py-2 rounded-lg font-semibold text-sm transition" style="background-color: var(--gold-color); color: #1a120b;">เสนอราคา</button>
                    </div>
                </div>
            </div>

            <!-- Item 3 -->
            <div class="rounded-2xl border overflow-hidden shadow-xl flex flex-col justify-between" style="background-color: var(--card-bg); border-color: var(--gold-color);">
                <div class="h-56 bg-cover bg-center relative flex items-end p-4" style="background-image: url('https://images.unsplash.com/photo-1579783900882-c0d3dad7b119?auto=format&fit=crop&q=80&w=600')">
                    <span class="bg-black/70 text-white text-xs px-3 py-1 rounded-full backdrop-blur-sm">ประมูลสดในเว็บ / FB Page</span>
                </div>
                <div class="p-6 space-y-4 flex-1 flex flex-col justify-between">
                    <div>
                        <h3 class="font-serif font-bold text-xl mb-1">"Vibrant Retro Soul"</h3>
                        <p class="text-sm opacity-80">โดย ครูมายด์ (เวิร์กช็อปเพ้นท์)</p>
                        <div class="mt-4 flex justify-between text-sm">
                            <span class="opacity-75">ราคาประมูลปัจจุบัน:</span>
                            <span class="font-bold text-amber-400" id="bidPrice3">980 บาท</span>
                        </div>
                    </div>
                    <div class="flex gap-2">
                        <input type="number" id="bidInput3" placeholder="เสนอราคาเพิ่ม" class="flex-1 bg-transparent border rounded-lg px-3 py-2 text-sm focus:outline-none" style="border-color: var(--gold-color);">
                        <button onclick="placeBid(3)" class="px-4 py-2 rounded-lg font-semibold text-sm transition" style="background-color: var(--gold-color); color: #1a120b;">เสนอราคา</button>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Workshop Booking System (จองคิวเวิร์กช็อป) -->
    <section id="workshop" class="py-20 px-4" style="background-color: var(--card-bg);">
        <div class="max-w-3xl mx-auto space-y-8">
            <div class="text-center space-y-4">
                <span class="px-4 py-1 rounded-full text-xs font-bold uppercase border" style="border-color: var(--gold-color); color: var(--gold-color);">Workshop Reservation</span>
                <h2 class="text-3xl font-serif font-bold" style="color: var(--gold-color);">จองคิวเวิร์กช็อปศิลปะ</h2>
                <p class="opacity-80">เลือกคอร์สที่คุณสนใจ ผ่อนคลายสมอง และสร้างสรรค์ผลงานชิ้นเอกด้วยมือคุณเอง</p>
            </div>

            <form onsubmit="handleBooking(event)" class="space-y-6 border-2 p-8 rounded-2xl shadow-xl" style="border-color: var(--gold-color);">
                <div class="grid md:grid-cols-2 gap-6">
                    <div>
                        <label class="block text-sm font-semibold mb-2">ชื่อ - นามสกุล</label>
                        <input type="text" id="bookName" required class="w-full bg-transparent border rounded-lg px-4 py-3 focus:outline-none" style="border-color: var(--gold-color);" placeholder="กรอกชื่อของคุณ">
                    </div>
                    <div>
                        <label class="block text-sm font-semibold mb-2">เบอร์โทรศัพท์ / โซเชียล</label>
                        <input type="text" id="bookContact" required class="w-full bg-transparent border rounded-lg px-4 py-3 focus:outline-none" style="border-color: var(--gold-color);" placeholder="เบอร์โทร หรือ ไลน์ไอดี">
                    </div>
                </div>

                <div class="grid md:grid-cols-2 gap-6">
                    <div>
                        <label class="block text-sm font-semibold mb-2">เลือกคอร์สเวิร์กช็อป</label>
                        <select id="bookCourse" class="w-full bg-transparent border rounded-lg px-4 py-3 focus:outline-none cursor-pointer" style="border-color: var(--gold-color); background-color: var(--card-bg); color: var(--text-color);">
                            <option value="เพ้นท์ภาพแคนวาสธีมวิคตอเรีย (350.-)">🎨 เพ้นท์ภาพแคนวาสธีมวิคตอเรีย (350.-)</option>
                            <option value="เพ้นท์เสื้อแฟชั่นสีฉูดฉาด (450.-)">👕 เพ้นท์เสื้อแฟชั่นสีฉูดฉาด (450.-)</option>
                            <option value="ปั้นดินเผาเครื่องปั้นสไตล์กรีซ-โรมัน (500.-)">🏺 ปั้นดินเผาเครื่องปั้นสไตล์กรีซ-โรมัน (500.-)</option>
                        </select>
                    </div>
                    <div>
                        <label class="block text-sm font-semibold mb-2">วันที่ต้องการเข้าร่วม</label>
                        <input type="date" id="bookDate" required class="w-full bg-transparent border rounded-lg px-4 py-3 focus:outline-none" style="border-color: var(--gold-color); color-scheme: dark;">
                    </div>
                </div>

                <button type="submit" class="w-full py-4 rounded-xl font-bold text-lg shadow-xl transition transform hover:scale-[1.01]" style="background-color: var(--gold-color); color: #1a120b;">
                    ยืนยันการจองคิวเวิร์กช็อป
                </button>
            </form>
            <div id="bookingResult" class="hidden text-center p-4 rounded-xl border border-green-500 bg-green-900/20 text-green-300 font-semibold"></div>
        </div>
    </section>

    <!-- Cafe & Fashion Preview -->
    <section id="menu" class="py-20 px-4 max-w-6xl mx-auto">
        <div class="text-center space-y-4 mb-12">
            <span class="px-4 py-1 rounded-full text-xs font-bold uppercase border" style="border-color: var(--gold-color); color: var(--gold-color);">Menu & Fashion</span>
            <h2 class="text-3xl font-serif font-bold" style="color: var(--gold-color);">คาเฟ่เครื่องดื่ม & แฟชั่นเสื้อผ้า</h2>
            <p class="opacity-80">ลิ้มรสกาแฟพรีเมียมและเครื่องดื่มสูตรพิเศษ พร้อมช้อปเสื้อผ้าแฟชั่นสไตล์ผสมผสานยุคสมัย</p>
        </div>

        <div class="grid md:grid-cols-2 gap-12">
            <!-- Cafe Drinks -->
            <div class="space-y-6">
                <h3 class="text-2xl font-serif font-bold flex items-center space-x-3" style="color: var(--gold-color);">
                    <i class="fa-solid fa-mug-hot"></i> <span>Artisan Café Menu</span>
                </h3>
                <div class="space-y-4">
                    <div class="flex justify-between items-center p-4 rounded-xl border" style="background-color: var(--card-bg); border-color: var(--gold-color);">
                        <div>
                            <h4 class="font-bold">Victorian Rose Latte</h4>
                            <p class="text-xs opacity-75">ลาเต้หอมกลิ่นกุหลาบอ่อนๆ ละมุนใจ</p>
                        </div>
                        <span class="font-bold text-amber-400">120.-</span>
                    </div>
                    <div class="flex justify-between items-center p-4 rounded-xl border" style="background-color: var(--card-bg); border-color: var(--gold-color);">
                        <div>
                            <h4 class="font-bold">Olympus Cold Brew</h4>
                            <p class="text-xs opacity-75">กาแฟสกัดเย็นเข้มข้น สดชื่นตื่นเต็มตา</p>
                        </div>
                        <span class="font-bold text-amber-400">110.-</span>
                    </div>
                    <div class="flex justify-between items-center p-4 rounded-xl border" style="background-color: var(--card-bg); border-color: var(--gold-color);">
                        <div>
                            <h4 class="font-bold">Vibrant Sunset Mocktail</h4>
                            <p class="text-xs opacity-75">ม็อกเทลสีสันฉูดฉาด ซ่าสดชื่น คลายร้อน</p>
                        </div>
                        <span class="font-bold text-amber-400">130.-</span>
                    </div>
                </div>
            </div>

            <!-- Fashion & Apparel -->
            <div class="space-y-6">
                <h3 class="text-2xl font-serif font-bold flex items-center space-x-3" style="color: var(--gold-color);">
                    <i class="fa-solid fa-shirt"></i> <span>Fashion & Apparel</span>
                </h3>
                <div class="space-y-4">
                    <div class="flex justify-between items-center p-4 rounded-xl border" style="background-color: var(--card-bg); border-color: var(--gold-color);">
                        <div>
                            <h4 class="font-bold">Neo-Victorian Lace Blouse</h4>
                            <p class="text-xs opacity-75">เสื้อลูกไม้ผสมผสานความโมเดิร์นคลาสสิก</p>
                        </div>
                        <span class="font-bold text-amber-400">890.-</span>
                    </div>
                    <div class="flex justify-between items-center p-4 rounded-xl border" style="background-color: var(--card-bg); border-color: var(--gold-color);">
                        <div>
                            <h4 class="font-bold">Greco-Roman Draped Tunic</h4>
                            <p class="text-xs opacity-75">เสื้อคลุมผ้าทิ้งตัวสไตล์เทพเจ้ากรีก</p>
                        </div>
                        <span class="font-bold text-amber-400">950.-</span>
                    </div>
                    <div class="flex justify-between items-center p-4 rounded-xl border" style="background-color: var(--card-bg); border-color: var(--gold-color);">
                        <div>
                            <h4 class="font-bold">Vibrant Color-Pop Tote Bag</h4>
                            <p class="text-xs opacity-75">กระเป๋าผ้าแคนวาสเพ้นท์ลายศิลปะฉูดฉาด</p>
                        </div>
                        <span class="font-bold text-amber-400">450.-</span>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="py-12 border-t border-amber-600/30 text-center text-sm opacity-80" style="background-color: var(--card-bg);">
        <div class="max-w-6xl mx-auto px-4 space-y-4">
            <h2 class="text-2xl font-serif font-bold" style="color: var(--gold-color);">ROGAFRY CAFÉ & GALLERY</h2>
            <p>เปิดให้บริการวันพฤหัสบดี - อังคาร เวลา 07.30 - 22.00 น. (หยุดวันพุธ)</p>
            <div class="flex justify-center space-x-6 pt-2 text-xl">
                <a href="#" class="hover:opacity-75"><i class="fa-brands fa-facebook"></i></a>
                <a href="#" class="hover:opacity-75"><i class="fa-brands fa-instagram"></i></a>
                <a href="#" class="hover:opacity-75"><i class="fa-brands fa-line"></i></a>
            </div>
            <p class="text-xs opacity-50 pt-4">© 2026 Rogafry Café. All rights reserved.</p>
        </div>
    </footer>

    <!-- JavaScript Interactions -->
    <script>
        // 1. Theme Switcher Function
        function changeTheme(themeName) {
            const body = document.getElementById('bodyTheme');
            body.className = `theme-${themeName}`;
        }

        // 2. Art Therapy Canvas Script
        const canvas = document.getElementById('therapyCanvas');
        const ctx = canvas.getContext('2d');
        let painting = false;

        function startPosition(e) {
            painting = true;
            draw(e);
        }

        function finishedPosition() {
            painting = false;
            ctx.beginPath();
        }

        function draw(e) {
            if (!painting) return;
            ctx.lineWidth = 12;
            ctx.lineCap = 'round';
            ctx.strokeStyle = document.getElementById('brushColor').value;

            const rect = canvas.getBoundingClientRect();
            let x = (e.clientX || e.touches[0].clientX) - rect.left;
            let y = (e.clientY || e.touches[0].clientY) - rect.top;

            ctx.lineTo(x, y);
            ctx.stroke();
            ctx.beginPath();
            ctx.moveTo(x, y);
        }

        canvas.addEventListener('mousedown', startPosition);
        canvas.addEventListener('mouseup', finishedPosition);
        canvas.addEventListener('mousemove', draw);

        canvas.addEventListener('touchstart', startPosition);
        canvas.addEventListener('touchend', finishedPosition);
        canvas.addEventListener('touchmove', draw);

        function clearCanvas() {
            ctx.clearRect(0, 0, canvas.width, canvas.height);
        }

        // 3. Live Bid Simulation
        function placeBid(id) {
            const input = document.getElementById(`bidInput${id}`);
            const priceEl = document.getElementById(`bidPrice${id}`);
            const val = parseInt(input.value);
            if (val && val > 0) {
                priceEl.innerText = val.toLocaleString() + ' บาท';
                alert('เสนอราคาสำเร็จ! ขอบคุณที่เป็นส่วนหนึ่งในคอมมูนิตี้ศิลปะ Rogafry');
                input.value = '';
            } else {
                alert('กรุณากรอกตัวเลขราคาที่ต้องการเสนอประมูลให้ถูกต้องครับ');
            }
        }

        // 4. Workshop Booking Handler
        function handleBooking(e) {
            e.preventDefault();
            const name = document.getElementById('bookName').value;
            const course = document.getElementById('bookCourse').value;
            const date = document.getElementById('bookDate').value;
            const resBox = document.getElementById('bookingResult');
            
            resBox.innerHTML = `🎉 ขอบคุณคุณ <strong>${name}</strong> สำหรับการจองคิวเวิร์กช็อป <strong>${course}</strong> ในวันที่ <strong>${date}</strong> เรียบร้อยแล้ว! ทางร้านจะติดต่อกลับเพื่อยืนยันคิวผ่านช่องทางที่คุณให้ไว้ครับ`;
            resBox.classList.remove('hidden');
            e.target.reset();
        }
    </script>
</body>
</html>
