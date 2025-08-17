<!DOCTYPE html>
<html lang="vi">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Thông Tin Cá Nhân Của Phạm Cao Phong</title>
    <!-- Tải Tailwind CSS từ CDN để dễ dàng styling và responsive -->
    <script src="https://cdn.tailwindcss.com"></script>
    <style>
        /* Định nghĩa font chữ Inter cho toàn bộ trang */
        body {
            font-family: "Inter", sans-serif;
            /* Đây là nơi bạn có thể thay đổi URL ảnh nền của mình */
            background-image: url('[https://scontent.fsgn5-9.fna.fbcdn.net/v/t39.30808-6/501207992_122249941046205763_7111883970957905367_n.jpg?stp=cp6_dst-jpg_tt6&_nc_cat=102&ccb=1-7&_nc_sid=6ee11a&_nc_ohc=lb_LOcvG8KoQ7kNvwE13v3k&_nc_oc=AdmZbJnLzcwLfkxII_xrvjtIR646-YUHsN_LXJHwkS5X4839n94HeJ_efLlQqkEb8jCedaMlu_5Er-TZxNVNp3fg&_nc_zt=23&_nc_ht=scontent.fsgn5-9.fna&_nc_gid=ZXsh4lx1UGGLzFl0KsiqcA&oh=00_AfWS8_39Ix8IRFplUiPX9haaPZ7SbRHvUIztXVLqVN9VHA&oe=68A64202](https://scontent.fsgn5-9.fna.fbcdn.net/v/t39.30808-6/501207992_122249941046205763_7111883970957905367_n.jpg?stp=cp6_dst-jpg_tt6&_nc_cat=102&ccb=1-7&_nc_sid=6ee11a&_nc_ohc=lb_LOcvG8KoQ7kNvwE13v3k&_nc_oc=AdmZbJnLzcwLfkxII_xrvjtIR646-YUHsN_LXJHwkS5X4839n94HeJ_efLlKqkEb8jCedaMlu_5Er-TZxNVNp3fg&_nc_zt=23&_nc_ht=scontent.fsgn5-9.fna&_nc_gid=lOx7i34Q8YYNnhWnrZUfgw&oh=00_AfVzRb7DJGWLHMfmqyrkfLBl5deEzkQFbij-G3gn-LgmLA&oe=68A64202)');
            background-size: cover; /* Đảm bảo ảnh bao phủ toàn bộ màn hình */
            background-position: center; /* Căn giữa ảnh nền */
            background-attachment: fixed; /* Giữ ảnh nền cố định khi cuộn */
            margin: 0;
            overflow: hidden; /* Ẩn thanh cuộn để hiệu ứng tuyết không bị cắt */
        }

        /* Lớp phủ (overlay) điều khiển độ đậm của background */
        #background-overlay {
            position: fixed; /* Giữ lớp phủ cố định trên màn hình */
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0, 0, 0, 0.7); /* Mặc định: nền đen đậm */
            z-index: 0; /* Nằm dưới nội dung */
            transition: background-color 0.5s ease; /* Hiệu ứng chuyển đổi mượt mà */
        }

        /* Vùng chứa bông tuyết */
        #snowflake-container {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            pointer-events: none; /* Không cho phép tương tác với chuột */
            z-index: 5; /* Nằm trên lớp phủ nền nhưng dưới nội dung chính */
        }

        /* Vùng bọc nội dung chính, đảm bảo nội dung nằm trên lớp phủ và được căn giữa */
        .content-wrapper {
            position: relative;
            z-index: 10; /* Nằm trên lớp phủ và bông tuyết */
            display: flex;
            flex-direction: column; /* Cho phép các phần tử con xếp dọc */
            justify-content: center; /* Căn giữa theo chiều ngang */
            align-items: center; /* Căn giữa theo chiều dọc */
            min-height: 100vh; /* Chiếm toàn bộ chiều cao màn hình */
            padding: 1rem; /* Padding cho các thiết bị di động */
        }

        /* Hộp nội dung chính (phần trắng) */
        #main-content-box {
            /* Mặc định: rất trong suốt và mờ như sương mù */
            background-color: rgba(255, 255, 255, 0.05); /* Rất trong suốt (5% độ mờ) */
            backdrop-filter: blur(20px); /* Làm mờ mạnh hơn để tạo hiệu ứng sương mù */
            border: 1px solid rgba(255, 255, 255, 0.1); /* Đường viền mỏng, trong suốt */
            transition: background-color 0.5s ease, backdrop-filter 0.5s ease, border-color 0.5s ease; /* Hiệu ứng chuyển đổi mượt mà */
        }

        /* Tăng cường độ đậm của chữ và hiệu ứng đổ bóng để nổi bật hơn */
        h1, h2, h3, strong {
            color: #1a202c; /* Màu chữ rất đậm, gần đen */
            text-shadow: 0 0 10px rgba(255, 255, 255, 1), /* Bóng sáng mạnh nhất, gần như màu trắng */
                         0 0 20px rgba(255, 255, 255, 0.8), /* Lớp bóng lớn hơn, mờ hơn */
                         0 0 30px rgba(255, 255, 255, 0.6); /* Lớp bóng lớn nhất, mờ nhất, tạo hiệu ứng phát sáng */
        }
        p, ul, li {
            color: #2d3748; /* Màu chữ tiêu chuẩn đậm hơn */
            text-shadow: 0 0 7px rgba(255, 255, 255, 0.9), /* Bóng sáng mạnh hơn */
                         0 0 12px rgba(255, 255, 255, 0.7); /* Thêm lớp bóng lớn hơn */
        }

        /* ---- CSS cho hiệu ứng sóng biển ---- */
        .wave-contact-section {
            position: relative;
            overflow: hidden; /* Quan trọng để sóng không tràn ra ngoài */
            border-radius: 0.75rem; /* rounded-xl */
            box-shadow: 0 10px 15px -3px rgba(0, 0, 0, 0.1), 0 4px 6px -2px rgba(0, 0, 0, 0.05); /* shadow-lg */
            min-height: 200px; /* Chiều cao tối thiểu để chứa sóng */
            display: flex;
            align-items: center;
            justify-content: center;
            background-color: rgba(255, 255, 255, 0.1); /* Nền nhẹ cho phần wave, sẽ bị lớp cha (main-content-box) làm mờ */
            /* backdrop-filter: blur(5px); */ /* Có thể thêm nếu muốn thêm mờ cho riêng phần này */
        }

        .wave-background {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            overflow: hidden;
        }

        .wave {
            position: absolute;
            width: 200%; /* Rộng hơn container để tạo hiệu ứng liên tục */
            height: 100px; /* Chiều cao trực quan của sóng */
            background-repeat: repeat-x;
            background-position: left bottom;
            opacity: 0.6;
            animation: wave-animation 10s linear infinite; /* Animation chính cho sóng */
        }

        /* Các lớp sóng khác nhau để tạo độ sâu */
        .wave1 {
            background-image: url('data:image/svg+xml;utf8,<svg viewBox="0 0 1440 320" xmlns="http://www.w3.org/2000/svg"><path fill="%2300BFFF" fill-opacity="0.7" d="M0,192L48,192C96,192,192,192,288,181.3C384,171,480,149,576,160C672,171,768,213,864,213.3C960,213,1056,171,1152,165.3C1248,160,1344,192,1392,208L1440,224L1440,320L1392,320C1344,320,1248,320,1152,320C1056,320,960,320,864,320C768,320,672,320,576,320C480,320,384,320,288,320C192,320,96,320,48,320L0,320Z"></path></svg>');
            height: 120px; /* Sóng lớn hơn */
            animation-duration: 15s; /* Chuyển động chậm hơn */
            z-index: 3; /* Nằm trên cùng */
            bottom: 0px;
        }

        .wave2 {
            background-image: url('data:image/svg+xml;utf8,<svg viewBox="0 0 1440 320" xmlns="http://www.w3.org/2000/svg"><path fill="%2387CEFA" fill-opacity="0.6" d="M0,160L48,170.7C96,181,192,203,288,202.7C384,203,480,181,576,154.7C672,128,768,96,864,96C960,96,1056,128,1152,149.3C1248,171,1344,181,1392,186.7L1440,192L1440,320L1392,320C1344,320,1248,320,1152,320C1056,320,960,320,864,320C768,320,672,320,576,320C480,320,384,320,288,320C192,320,96,320,48,320L0,320Z"></path></svg>');
            height: 100px; /* Sóng trung bình */
            animation-duration: 20s; /* Chuyển động trung bình */
            z-index: 2; /* Nằm giữa */
            bottom: 5px; /* Cao hơn một chút so so với sóng 1 */
            opacity: 0.5;
        }

        .wave3 {
            background-image: url('data:image/svg+xml;utf8,<svg viewBox="0 0 1440 320" xmlns="http://www.w3.org/2000/svg"><path fill="%23ADD8E6" fill-opacity="0.5" d="M0,224L48,213.3C96,203,192,181,288,181.3C384,181,480,203,576,218.7C672,235,768,245,864,240C960,235,1056,219,1152,208C1248,197,1344,197,1392,197.3L1440,197L1440,320L1392,320C1344,320,1248,320,1152,320C1056,320,960,320,864,320C768,320,672,320,576,320C480,320,384,320,288,320C192,320,96,320,48,320L0,320Z"></path></svg>');
            height: 80px; /* Sóng nhỏ hơn */
            animation-duration: 25s; /* Chuyển động nhanh hơn một chút */
            z-index: 1; /* Nằm dưới cùng */
            bottom: 10px; /* Cao hơn nữa so với sóng 2 */
            opacity: 0.4;
        }

        @keyframes wave-animation {
            0% { background-position-x: 0; }
            100% { background-position-x: 1440px; } /* Đảm bảo vòng lặp liên tục */
        }

        /* CSS cho hệ thống đánh giá sao */
        .star-rating {
            display: flex;
            flex-direction: row-reverse; /* Đảo ngược thứ tự để sao 5 ở bên phải */
            justify-content: center;
            gap: 0.25rem; /* Khoảng cách giữa các sao */
        }

        .star-rating input[type="radio"] {
            display: none; /* Ẩn radio button gốc */
        }

        .star-rating label {
            cursor: pointer;
            font-size: 2.5rem; /* Kích thước sao */
            color: #ccc; /* Màu sao mặc định (chưa chọn) */
            transition: color 0.2s ease-in-out;
            /* SVG icon for star */
            width: 2.5rem; /* Đảm bảo kích thước SVG khớp với font-size */
            height: 2.5rem;
        }

        .star-rating svg {
            fill: currentColor; /* Dùng màu từ parent (label) */
            stroke: currentColor; /* Dùng màu từ parent (label) */
            stroke-width: 0; /* Không có viền */
        }

        /* Màu khi di chuột qua hoặc đã chọn */
        .star-rating input[type="radio"]:checked ~ label,
        .star-rating label:hover,
        .star-rating label:hover ~ label {
            color: #ffc107; /* Màu vàng cam khi chọn hoặc hover */
        }

        /* Màu khi di chuột ra khỏi sao đã chọn (để giữ màu vàng) */
        .star-rating input[type="radio"]:checked + label:hover,
        .star-rating input[type="radio"]:checked ~ label:hover,
        .star-rating input[type="radio"]:checked ~ label:hover ~ label,
        .star-rating label:hover ~ input[type="radio"]:checked ~ label {
            color: #ffc107;
        }

        /* ---- CSS cho hiệu ứng bông tuyết ---- */
        .snowflake {
            position: absolute;
            background-color: #fff; /* Màu trắng */
            border-radius: 50%; /* Hình tròn */
            opacity: 0; /* Bắt đầu với độ trong suốt bằng 0 */
            animation: snowflake-fall linear infinite;
        }

        @keyframes snowflake-fall {
            0% {
                transform: translateY(-10vh) translateX(0); /* Bắt đầu từ trên cao */
                opacity: 0;
            }
            10% {
                opacity: 0.8; /* Hiện rõ dần */
            }
            90% {
                opacity: 0.8;
            }
            100% {
                transform: translateY(100vh) translateX(var(--x-drift)); /* Rơi xuống và trôi ngang */
                opacity: 0; /* Biến mất khi chạm đáy */
            }
        }
    </style>
</head>
<body>
    <div id="background-overlay"></div> <!-- Lớp phủ nền động -->
    <div id="snowflake-container"></div> <!-- Vùng chứa bông tuyết -->

    <div class="content-wrapper">
        <div id="main-content-box" class="rounded-xl shadow-lg p-8 md:p-12 max-w-4xl w-full mx-auto">
            <!-- Phần Header - Giới thiệu chung -->
            <header class="text-center mb-10">
                <h1 class="text-4xl md:text-5xl font-extrabold text-blue-800 mb-2">
                    <span class="text-orange-600">Phạm Cao Phong</span>
                </h1>
                <p class="text-lg md:text-xl text-gray-600">
                    Đam mê lập trình web
                </p>
            </header>

            <!-- Phần Thông tin cơ bản -->
            <section class="mb-10">
                <h2 class="text-3xl font-bold text-gray-800 mb-4 border-b-2 border-blue-500 pb-2">
                    Thông Tin Cơ Bản
                </h2>
                <div class="space-y-2 text-gray-700 leading-relaxed">
                    <p><strong>Họ và Tên:</strong> Phạm Cao Phong</p>
                    <p><strong>Quê quán:</strong> Thành phố Hồ Chí Minh</p>
                </div>
            </section>

            <!-- Phần Giới thiệu bản thân -->
            <section class="mb-10">
                <h2 class="text-3xl font-bold text-gray-800 mb-4 border-b-2 border-blue-500 pb-2">
                    Về Tôi
                </h2>
                <p class="text-gray-700 leading-relaxed">
                    Xin chào! Tôi là Phạm Cao Phong, một học sinh với **đam mê mãnh liệt về lập trình web**. Tôi luôn tìm tòi và khám phá những điều thú vị trong lĩnh vực này, đồng thời không ngừng học hỏi để nâng cao kiến thức và kỹ năng của mình.
                </p>
                <p class="text-gray-700 leading-relaxed mt-4">
                    Sở thích của tôi bao gồm [Liệt kê sở thích, ví dụ: đọc sách về công nghệ, chơi game, đi du lịch, tập gym]. Tôi luôn tin rằng việc cân bằng giữa việc học và giải trí sẽ mang lại hiệu suất tốt nhất.
                </p>
            </section>

            <!-- Phần Kỹ năng -->
            <section class="mb-10">
                <h2 class="text-3xl font-bold text-gray-800 mb-4 border-b-2 border-blue-500 pb-2">
                    Kỹ Năng
                </h2>
                <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
                    <div>
                        <h3 class="text-xl font-semibold text-gray-700 mb-3">Kỹ năng chuyên môn</h3>
                        <ul class="list-disc list-inside space-y-2 text-gray-600">
                            <li><strong>Lập trình:</strong> Python</li>
                        </ul>
                    </div>
                    <div>
                        <h3 class="text-xl font-semibold text-gray-700 mb-3">Kỹ năng mềm</h3>
                        <ul class="list-disc list-inside space-y-2 text-gray-600">
                            <li>Giải quyết vấn đề</li>
                            <li>Tư duy phản biện</li>
                            <li>Giao tiếp hiệu quả</li>
                            <li>Làm việc nhóm</li>
                            <li>Khả năng thích nghi</li>
                        </ul>
                    </div>
                </div>
            </section>

            <!-- Phần Liên hệ tạo web với hiệu ứng sóng biển -->
            <section class="mb-10">
                <h2 class="text-3xl font-bold text-gray-800 mb-4 border-b-2 border-blue-500 pb-2">
                    Nhu Cầu Tạo Web
                </h2>
                <div class="wave-contact-section">
                    <div class="wave-background">
                        <div class="wave wave1"></div>
                        <div class="wave wave2"></div>
                        <div class="wave wave3"></div>
                    </div>
                    <div class="relative z-10 text-center p-4">
                        <p class="text-2xl md:text-3xl font-bold text-blue-900 mb-4">
                            Ai có nhu cầu tạo web
                        </p>
                        <p class="text-3xl md:text-4xl font-extrabold text-blue-900">
                            Liên hệ: 0359710381
                        </p>
                    </div>
                </div>
            </section>

            <!-- Phần Thông tin liên hệ và phản hồi khách hàng -->
            <section class="mb-10">
                <h2 class="text-3xl font-bold text-gray-800 mb-4 border-b-2 border-blue-500 pb-2">
                    Thông Tin Liên Hệ & Phản Hồi Khách Hàng
                </h2>
                <form id="customerFeedbackForm" class="space-y-4 text-gray-700">
                    <p class="text-center text-lg font-semibold text-gray-800">
                        Vui lòng để lại thông tin và đánh giá của bạn:
                    </p>
                    <div>
                        <label for="clientName" class="block text-lg font-semibold mb-1">Họ và tên:</label>
                        <input type="text" id="clientName" name="clientName" placeholder="Nhập họ và tên của bạn" class="w-full p-2 border border-gray-300 rounded-md focus:outline-none focus:ring-2 focus:ring-blue-500 bg-white bg-opacity-70" required>
                    </div>
                    <div>
                        <label for="clientPhone" class="block text-lg font-semibold mb-1">Số điện thoại:</label>
                        <input type="tel" id="clientPhone" name="clientPhone" placeholder="Nhập số điện thoại của bạn" class="w-full p-2 border border-gray-300 rounded-md focus:outline-none focus:ring-2 focus:ring-blue-500 bg-white bg-opacity-70" required>
                    </div>
                    <div class="grid grid-cols-1 md:grid-cols-2 gap-4">
                        <div>
                            <label for="clientAge" class="block text-lg font-semibold mb-1">Tuổi:</label>
                            <input type="number" id="clientAge" name="clientAge" placeholder="Tuổi của bạn" class="w-full p-2 border border-gray-300 rounded-md focus:outline-none focus:ring-2 focus:ring-blue-500 bg-white bg-opacity-70" min="1" max="120">
                        </div>
                        <div>
                            <label for="clientGender" class="block text-lg font-semibold mb-1">Giới tính:</label>
                            <select id="clientGender" name="clientGender" class="w-full p-2 border border-gray-300 rounded-md focus:outline-none focus:ring-2 focus:ring-blue-500 bg-white bg-opacity-70">
                                <option value="">Chọn giới tính</option>
                                <option value="nam">Nam</option>
                                <option value="nu">Nữ</option>
                                <option value="khac">Khác</option>
                            </select>
                        </div>
                    </div>

                    <div class="text-center pt-4 border-t border-gray-300">
                        <label class="block text-lg font-semibold mb-2">Đánh giá của bạn:</label>
                        <div class="star-rating">
                            <input type="radio" id="star5" name="rating" value="5" required><label for="star5" title="5 sao">
                                <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24"><path d="M12 17.27L18.18 21l-1.64-7.03L22 9.24l-7.19-.61L12 2 9.19 8.63L2 9.24l5.46 4.73L5.82 21z"/></svg>
                            </label>
                            <input type="radio" id="star4" name="rating" value="4"><label for="star4" title="4 sao">
                                <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24"><path d="M12 17.27L18.18 21l-1.64-7.03L22 9.24l-7.19-.61L12 2 9.19 8.63L2 9.24l5.46 4.73L5.82 21z"/></svg>
                            </label>
                            <input type="radio" id="star3" name="rating" value="3"><label for="star3" title="3 sao">
                                <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24"><path d="M12 17.27L18.18 21l-1.64-7.03L22 9.24l-7.19-.61L12 2 9.19 8.63L2 9.24l5.46 4.73L5.82 21z"/></svg>
                            </label>
                            <input type="radio" id="star2" name="rating" value="2"><label for="star2" title="2 sao">
                                <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24"><path d="M12 17.27L18.18 21l-1.64-7.03L22 9.24l-7.19-.61L12 2 9.19 8.63L2 9.24l5.46 4.73L5.82 21z"/></svg>
                            </label>
                            <input type="radio" id="star1" name="rating" value="1"><label for="star1" title="1 sao">
                                <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24"><path d="M12 17.27L18.18 21l-1.64-7.03L22 9.24l-7.19-.61L12 2 9.19 8.63L2 9.24l5.46 4.73L5.82 21z"/></svg>
                            </label>
                        </div>
                    </div>
                    <div>
                        <label for="feedbackMessage" class="block text-lg font-semibold mb-1">Phản hồi của bạn:</label>
                        <textarea id="feedbackMessage" name="feedbackMessage" rows="5" placeholder="Nhập phản hồi của bạn về trang web..." class="w-full p-2 border border-gray-300 rounded-md focus:outline-none focus:ring-2 focus:ring-blue-500 bg-white bg-opacity-70" required></textarea>
                    </div>
                    <button type="submit" class="w-full bg-blue-600 text-white font-bold py-3 px-4 rounded-md hover:bg-blue-700 transition duration-300">
                        Gửi Phản Hồi
                    </button>
                </form>
            </section>

            <!-- Phần Liên hệ cá nhân (giữ nguyên) -->
            <section class="text-center">
                <h2 class="text-3xl font-bold text-gray-800 mb-4 border-b-2 border-blue-500 pb-2 inline-block">
                    Liên Hệ Cá Nhân
                </h2>
                <p class="text-gray-700 leading-relaxed mt-4">
                    Nếu bạn có bất kỳ câu hỏi nào, muốn thảo luận về một dự án, hay đơn giản là muốn trò chuyện, đừng ngần ngại liên hệ với tôi qua:
                </p>
                <div class="mt-6 text-xl space-y-2">
                    <p><strong class="text-blue-700">Điện thoại:</strong> <span class="text-gray-700">0359710381</span></p>
                    <p><strong class="text-blue-700">Facebook:</strong> <a href="https://www.facebook.com/pham.cao. phong.866751" target="_blank" class="text-gray-700 hover:underline">Phạm Cao Phong</a></p>
                    <p><strong class="text-blue-700">Email:</strong> <a href="mailto:phamcaophong177@gmail.com" class="text-gray-700 hover:underline">phamcaophong177@gmail.com</a></p>
                </div>
            </section>
        </div>
    </div>

    <script>
        // Lấy tham chiếu đến các phần tử cần tương tác
        const mainContentBox = document.getElementById('main-content-box');
        const backgroundOverlay = document.getElementById('background-overlay');
        const customerFeedbackForm = document.getElementById('customerFeedbackForm'); // Đã đổi ID form
        const snowflakeContainer = document.getElementById('snowflake-container'); // Lấy vùng chứa bông tuyết

        // Thêm sự kiện khi di chuột vào hộp nội dung chính
        mainContentBox.addEventListener('mouseenter', () => {
            // Khi chuột vào: background sáng hơn, nội dung rõ hơn
            backgroundOverlay.style.backgroundColor = 'rgba(0, 0, 0, 0.3)'; /* Nền ít đậm hơn */
            mainContentBox.style.backgroundColor = 'rgba(255, 255, 255, 1)'; /* Hoàn toàn mờ đục */
            mainContentBox.style.backdropFilter = 'blur(0px)'; /* Không làm mờ */
            mainContentBox.style.borderColor = 'rgba(255, 255, 255, 1)'; /* Viền rõ ràng hơn */
        });

        // Thêm sự kiện khi di chuột ra khỏi hộp nội dung chính
        mainContentBox.addEventListener('mouseleave', () => {
            // Khi chuột ra: background đậm lên, nội dung mờ tan như sương mù
            backgroundOverlay.style.backgroundColor = 'rgba(0, 0, 0, 0.7)'; /* Nền đậm hơn */
            mainContentBox.style.backgroundColor = 'rgba(255, 255, 255, 0.05)'; /* Mờ tan (5% mờ) */
            mainContentBox.style.backdropFilter = 'blur(20px)'; /* Mờ mạnh hơn để tạo sương mù */
            mainContentBox.style.borderColor = 'rgba(255, 255, 255, 0.1)'; /* Viền mờ hơn */
        });

        // Xử lý gửi thông tin khách hàng và phản hồi
        customerFeedbackForm.addEventListener('submit', (event) => {
            event.preventDefault(); // Ngăn form gửi đi theo cách truyền thống

            // Lấy thông tin khách hàng
            const clientName = document.getElementById('clientName').value;
            const clientPhone = document.getElementById('clientPhone').value;
            const clientAge = document.getElementById('clientAge').value;
            const clientGender = document.getElementById('clientGender').value;

            // Lấy thông tin phản hồi
            const rating = document.querySelector('input[name="rating"]:checked');
            const feedbackMessage = document.getElementById('feedbackMessage').value;

            // Xây dựng tiêu đề email
            let subject = `Phản hồi từ khách hàng: ${clientName} - ${clientPhone}`;

            // Xây dựng nội dung email
            let body = `THÔNG TIN KHÁCH HÀNG:\n`;
            body += `Họ và tên: ${clientName}\n`;
            body += `Số điện thoại: ${clientPhone}\n`;
            body += `Tuổi: ${clientAge || 'Không cung cấp'}\n`; // Nếu không điền tuổi, hiển thị 'Không cung cấp'
            body += `Giới tính: ${clientGender || 'Không cung cấp'}\n\n`; // Nếu không chọn giới tính, hiển thị 'Không cung cấp'

            body += `PHẢN HỒI & ĐÁNH GIÁ:\n`;
            body += `Đánh giá: ${rating ? rating.value + " sao" : "Không đánh giá"}\n`;
            body += `Nội dung phản hồi:\n${feedbackMessage}`;

            // Mã hóa nội dung để tránh lỗi URL
            const mailtoLink = `mailto:phamcaophong177@gmail.com?subject=${encodeURIComponent(subject)}&body=${encodeURIComponent(body)}`;

            // Mở ứng dụng email mặc định của người dùng
            window.location.href = mailtoLink;

            // Tùy chọn: Hiển thị thông báo cho người dùng
            alert('Cảm ơn bạn đã gửi thông tin và phản hồi! Ứng dụng email của bạn sẽ mở ra để hoàn tất việc gửi.');

            // Tùy chọn: Xóa form sau khi gửi
            // customerFeedbackForm.reset();
        });

        // ---- JavaScript cho hiệu ứng bông tuyết ----
        function createSnowflake() {
            const snowflake = document.createElement('div');
            snowflake.classList.add('snowflake');

            // Kích thước bông tuyết ngẫu nhiên (nhỏ và vừa)
            const size = Math.random() * 3 + 2; // Từ 2px đến 5px
            snowflake.style.width = `${size}px`;
            snowflake.style.height = `${size}px`;

            // Vị trí bắt đầu ngẫu nhiên (từ 0% đến 100% chiều rộng màn hình)
            snowflake.style.left = `${Math.random() * 100}vw`;

            // Tốc độ rơi ngẫu nhiên
            const duration = Math.random() * 10 + 5; // Từ 5 đến 15 giây
            snowflake.style.animationDuration = `${duration}s`;

            // Độ trôi ngang ngẫu nhiên
            const xDrift = (Math.random() - 0.5) * 100; // Từ -50vw đến 50vw
            snowflake.style.setProperty('--x-drift', `${xDrift}vw`);

            // Độ trễ animation ngẫu nhiên để bông tuyết xuất hiện không đồng loạt
            snowflake.style.animationDelay = `-${Math.random() * duration}s`; // Bắt đầu từ giữa animation

            snowflakeContainer.appendChild(snowflake);

            // Xóa bông tuyết sau khi rơi xong để tối ưu hiệu suất
            setTimeout(() => {
                snowflake.remove();
            }, duration * 1000);
        }

        // Tạo bông tuyết mới liên tục
        // Điều chỉnh tần suất tạo bông tuyết để có mật độ phù hợp
        setInterval(createSnowflake, 200); // Tạo một bông tuyết mới mỗi 200ms
    </script>
</body>
</html>
