YPE html><!DOCT
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>智能果林监测App - 原型展示</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        .gradient-bg {
            background: linear-gradient(135deg, #4CAF50 0%, #2E7D32 100%);
        }
        .iphone-frame {
            width: 390px;
            height: 844px;
            border-radius: 50px;
            overflow: hidden;
            position: relative;
            box-shadow: 0 0 20px rgba(0,0,0,0.2);
            background: #000;
            margin: 2rem;
        }
        .screen {
            width: 100%;
            height: 100%;
            background: #fff;
            border-radius: 40px;
            overflow: hidden;
            position: relative;
        }
        .status-bar {
            height: 44px;
            background: #000;
            color: white;
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 0 20px;
            font-size: 14px;
        }
        .tab-bar {
            height: 83px;
            background: rgba(255,255,255,0.9);
            backdrop-filter: blur(10px);
            position: absolute;
            bottom: 0;
            width: 100%;
            display: flex;
            justify-content: space-around;
            align-items: center;
            border-top: 1px solid #eee;
        }
        .tab-item {
            display: flex;
            flex-direction: column;
            align-items: center;
            color: #666;
        }
        .tab-item.active {
            color: #007AFF;
        }
        .tab-icon {
            font-size: 24px;
            margin-bottom: 4px;
        }
        .tab-label {
            font-size: 10px;
        }
        .card-hover {
            transition: transform 0.2s;
        }
        .card-hover:hover {
            transform: translateY(-2px);
        }
        .chat-bubble {
            max-width: 80%;
            border-radius: 1rem;
            padding: 0.75rem 1rem;
            margin-bottom: 0.5rem;
        }
        .chat-bubble.user {
            background-color: #E3F2FD;
            margin-left: auto;
            border-bottom-right-radius: 0.25rem;
        }
        .chat-bubble.expert, .chat-bubble.service {
            background-color: #F5F5F5;
            margin-right: auto;
            border-bottom-left-radius: 0.25rem;
        }
        .prototype-tab {
            display: none;
        }
        .prototype-tab.active {
            display: block;
        }
        .tab-button {
            padding: 0.5rem 1rem;
            border-radius: 0.5rem;
            cursor: pointer;
            transition: all 0.2s;
        }
        .tab-button.active {
            background-color: #4CAF50;
            color: white;
        }
    </style>
</head>
<body class="bg-gray-100 p-8">
    <div class="max-w-7xl mx-auto">
        <h1 class="text-3xl font-bold mb-8 text-center">智能果林监测App - 原型展示</h1>
        
        <!-- 导航标签 -->
        <div class="flex justify-center space-x-4 mb-8">
            <button class="tab-button active" onclick="showTab('academy')">果林学堂</button>
            <button class="tab-button" onclick="showTab('knowledge')">知识详情</button>
            <button class="tab-button" onclick="showTab('expert')">专家咨询</button>
            <button class="tab-button" onclick="showTab('service')">客服咨询</button>
        </div>

        <!-- 果林学堂界面 -->
        <div id="academy" class="prototype-tab active">
            <div class="iphone-frame">
                <div class="screen">
                    <div class="status-bar">
                        <span>9:41</span>
                        <div class="flex space-x-2">
                            <i class="fas fa-signal"></i>
                            <i class="fas fa-wifi"></i>
                            <i class="fas fa-battery-full"></i>
                        </div>
                    </div>
                    <div class="p-4 space-y-6">
                        <!-- 果林知识卡片 -->
                        <div class="bg-white rounded-xl shadow-sm overflow-hidden card-hover">
                            <div class="p-4">
                                <div class="flex items-center justify-between mb-4">
                                    <h2 class="text-lg font-semibold text-gray-800">果林知识</h2>
                                    <a href="#" class="text-green-600 text-sm">查看全部 <i class="fas fa-chevron-right"></i></a>
                                </div>
                                <div class="grid grid-cols-2 gap-4">
                                    <div class="bg-gray-50 rounded-lg p-3">
                                        <img src="https://images.unsplash.com/photo-1516257984-1c7b0b5e5e5c?ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60" 
                                             class="w-full h-24 object-cover rounded-lg mb-2">
                                        <h3 class="text-sm font-medium text-gray-800">果树病虫害防治</h3>
                                        <p class="text-xs text-gray-500">了解常见病虫害及防治方法</p>
                                    </div>
                                    <div class="bg-gray-50 rounded-lg p-3">
                                        <img src="https://images.unsplash.com/photo-1516257984-1c7b0b5e5e5c?ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60" 
                                             class="w-full h-24 object-cover rounded-lg mb-2">
                                        <h3 class="text-sm font-medium text-gray-800">果树修剪技术</h3>
                                        <p class="text-xs text-gray-500">掌握正确的修剪时机和方法</p>
                                    </div>
                                </div>
                            </div>
                        </div>

                        <!-- 专家指导卡片 -->
                        <div class="bg-white rounded-xl shadow-sm overflow-hidden card-hover">
                            <div class="p-4">
                                <div class="flex items-center justify-between mb-4">
                                    <h2 class="text-lg font-semibold text-gray-800">专家指导</h2>
                                    <a href="#" class="text-green-600 text-sm">立即咨询 <i class="fas fa-chevron-right"></i></a>
                                </div>
                                <div class="flex items-center space-x-4 p-3 bg-gray-50 rounded-lg">
                                    <img src="https://images.unsplash.com/photo-1559839734-2b71ea197ec2?ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60" 
                                         class="w-16 h-16 rounded-full object-cover">
                                    <div>
                                        <h3 class="font-medium text-gray-800">张教授</h3>
                                        <p class="text-sm text-gray-500">果树栽培专家</p>
                                        <div class="flex items-center mt-1">
                                            <span class="text-yellow-400 text-sm">
                                                <i class="fas fa-star"></i>
                                                <i class="fas fa-star"></i>
                                                <i class="fas fa-star"></i>
                                                <i class="fas fa-star"></i>
                                                <i class="fas fa-star-half-alt"></i>
                                            </span>
                                            <span class="text-gray-500 text-xs ml-1">4.5</span>
                                        </div>
                                    </div>
                                </div>
                            </div>
                        </div>

                        <!-- 客服咨询卡片 -->
                        <div class="bg-white rounded-xl shadow-sm overflow-hidden card-hover">
                            <div class="p-4">
                                <div class="flex items-center justify-between mb-4">
                                    <h2 class="text-lg font-semibold text-gray-800">客服咨询</h2>
                                    <a href="#" class="text-green-600 text-sm">在线咨询 <i class="fas fa-chevron-right"></i></a>
                                </div>
                                <div class="bg-gray-50 rounded-lg p-4">
                                    <div class="flex items-center space-x-3">
                                        <div class="w-10 h-10 rounded-full bg-green-100 flex items-center justify-center">
                                            <i class="fas fa-headset text-green-600"></i>
                                        </div>
                                        <div>
                                            <h3 class="font-medium text-gray-800">24小时在线客服</h3>
                                            <p class="text-sm text-gray-500">随时解答您的疑问</p>
                                        </div>
                                    </div>
                                    <div class="mt-4 flex space-x-2">
                                        <button class="flex-1 bg-green-600 text-white py-2 px-4 rounded-lg text-sm">
                                            <i class="fas fa-comment-dots mr-1"></i> 在线咨询
                                        </button>
                                        <button class="flex-1 bg-gray-100 text-gray-800 py-2 px-4 rounded-lg text-sm">
                                            <i class="fas fa-phone-alt mr-1"></i> 电话咨询
                                        </button>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                    <div class="tab-bar">
                        <div class="tab-item">
                            <i class="fas fa-home tab-icon"></i>
                            <span class="tab-label">主页</span>
                        </div>
                        <div class="tab-item">
                            <i class="fas fa-tree tab-icon"></i>
                            <span class="tab-label">3D果林</span>
                        </div>
                        <div class="tab-item active">
                            <i class="fas fa-graduation-cap tab-icon"></i>
                            <span class="tab-label">果林学堂</span>
                        </div>
                        <div class="tab-item">
                            <i class="fas fa-user tab-icon"></i>
                            <span class="tab-label">我的</span>
                        </div>
                    </div>
                </div>
            </div>
        </div>

        <!-- 知识详情界面 -->
        <div id="knowledge" class="prototype-tab">
            <div class="iphone-frame">
                <div class="screen">
                    <div class="status-bar">
                        <span>9:41</span>
                        <div class="flex space-x-2">
                            <i class="fas fa-signal"></i>
                            <i class="fas fa-wifi"></i>
                            <i class="fas fa-battery-full"></i>
                        </div>
                    </div>
                    <div class="p-4">
                        <!-- 文章头部 -->
                        <div class="bg-white rounded-xl shadow-sm p-4 mb-4">
                            <img src="https://images.unsplash.com/photo-1516257984-1c7b0b5e5e5c?ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60" 
                                 class="w-full h-48 object-cover rounded-lg mb-4">
                            <div class="flex items-center justify-between mb-4">
                                <div class="flex items-center space-x-2">
                                    <img src="https://images.unsplash.com/photo-1559839734-2b71ea197ec2?ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60" 
                                         class="w-8 h-8 rounded-full object-cover">
                                    <span class="text-sm text-gray-600">张教授</span>
                                </div>
                                <span class="text-sm text-gray-500">2024-03-15</span>
                            </div>
                            <div class="flex space-x-4 text-gray-500 text-sm">
                                <span><i class="far fa-eye mr-1"></i> 1.2k</span>
                                <span><i class="far fa-thumbs-up mr-1"></i> 256</span>
                                <span><i class="far fa-comment mr-1"></i> 48</span>
                            </div>
                        </div>

                        <!-- 文章内容 -->
                        <div class="bg-white rounded-xl shadow-sm p-4">
                            <h2 class="text-lg font-semibold text-gray-800 mb-4">常见果树病虫害及防治方法</h2>
                            
                            <div class="space-y-4 text-gray-700">
                                <p>果树病虫害是影响果树生长和果实品质的重要因素。本文将介绍几种常见的果树病虫害及其防治方法。</p>
                                
                                <h3 class="font-medium text-gray-800 mt-6 mb-2">1. 蚜虫防治</h3>
                                <p>蚜虫是果树常见的害虫之一，主要危害嫩叶和嫩梢。防治方法：</p>
                                <ul class="list-disc pl-5 space-y-2">
                                    <li>定期检查果树，发现蚜虫及时处理</li>
                                    <li>使用生物农药进行防治</li>
                                    <li>保持果园通风透光</li>
                                </ul>

                                <h3 class="font-medium text-gray-800 mt-6 mb-2">2. 白粉病防治</h3>
                                <p>白粉病是果树常见的真菌性病害，主要危害叶片和果实。防治方法：</p>
                                <ul class="list-disc pl-5 space-y-2">
                                    <li>选择抗病品种</li>
                                    <li>合理施肥，增强树势</li>
                                    <li>发病初期及时喷药防治</li>
                                </ul>

                                <div class="mt-6 p-4 bg-green-50 rounded-lg">
                                    <h4 class="font-medium text-green-800 mb-2">专家建议</h4>
                                    <p class="text-green-700">建议在病虫害防治过程中，优先使用生物防治方法，减少化学农药的使用，保护生态环境。</p>
                                </div>
                            </div>
                        </div>
                    </div>
                    <div class="tab-bar">
                        <div class="tab-item">
                            <i class="fas fa-home tab-icon"></i>
                            <span class="tab-label">主页</span>
                        </div>
                        <div class="tab-item">
                            <i class="fas fa-tree tab-icon"></i>
                            <span class="tab-label">3D果林</span>
                        </div>
                        <div class="tab-item active">
                            <i class="fas fa-graduation-cap tab-icon"></i>
                            <span class="tab-label">果林学堂</span>
                        </div>
                        <div class="tab-item">
                            <i class="fas fa-user tab-icon"></i>
                            <span class="tab-label">我的</span>
                        </div>
                    </div>
                </div>
            </div>
        </div>

        <!-- 专家咨询界面 -->
        <div id="expert" class="prototype-tab">
            <div class="iphone-frame">
                <div class="screen">
                    <div class="status-bar">
                        <span>9:41</span>
                        <div class="flex space-x-2">
                            <i class="fas fa-signal"></i>
                            <i class="fas fa-wifi"></i>
                            <i class="fas fa-battery-full"></i>
                        </div>
                    </div>
                    <div class="p-4 pb-24">
                        <!-- 专家介绍卡片 -->
                        <div class="bg-white rounded-xl shadow-sm p-4 mb-4">
                            <div class="flex items-center space-x-4">
                                <img src="https://images.unsplash.com/photo-1559839734-2b71ea197ec2?ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60" 
                                     class="w-16 h-16 rounded-full object-cover">
                                <div>
                                    <h3 class="font-medium text-gray-800">张教授</h3>
                                    <p class="text-sm text-gray-500">果树栽培专家</p>
                                    <div class="flex items-center mt-1">
                                        <span class="text-yellow-400 text-sm">
                                            <i class="fas fa-star"></i>
                                            <i class="fas fa-star"></i>
                                            <i class="fas fa-star"></i>
                                            <i class="fas fa-star"></i>
                                            <i class="fas fa-star-half-alt"></i>
                                        </span>
                                        <span class="text-gray-500 text-xs ml-1">4.5</span>
                                    </div>
                                </div>
                            </div>
                            <div class="mt-4 text-sm text-gray-600">
                                <p>从事果树栽培研究20余年，擅长果树病虫害防治、果树修剪等技术指导。</p>
                            </div>
                        </div>

                        <!-- 聊天记录 -->
                        <div class="space-y-4">
                            <!-- 专家消息 -->
                            <div class="flex items-start space-x-2">
                                <img src="https://images.unsplash.com/photo-1559839734-2b71ea197ec2?ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60" 
                                     class="w-8 h-8 rounded-full object-cover">
                                <div class="chat-bubble expert">
                                    <p class="text-gray-800">您好！我是张教授，有什么可以帮到您的吗？</p>
                                    <span class="text-xs text-gray-500 mt-1 block">10:30</span>
                                </div>
                            </div>

                            <!-- 用户消息 -->
                            <div class="flex items-start justify-end space-x-2">
                                <div class="chat-bubble user">
                                    <p class="text-gray-800">您好，张教授！我的苹果树最近叶子发黄，不知道是什么原因？</p>
                                    <span class="text-xs text-gray-500 mt-1 block">10:32</span>
                                </div>
                            </div>

                            <!-- 专家消息 -->
                            <div class="flex items-start space-x-2">
                                <img src="https://images.unsplash.com/photo-1559839734-2b71ea197ec2?ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60" 
                                     class="w-8 h-8 rounded-full object-cover">
                                <div class="chat-bubble expert">
                                    <p class="text-gray-800">叶子发黄可能是由多种原因引起的，建议您先检查：</p>
                                    <ul class="list-disc pl-5 mt-2 text-gray-800">
                                        <li>土壤湿度是否合适</li>
                                        <li>是否有病虫害</li>
                                        <li>施肥情况</li>
                                    </ul>
                                    <p class="text-gray-800 mt-2">您可以拍几张照片发给我，我帮您具体分析一下。</p>
                                    <span class="text-xs text-gray-500 mt-1 block">10:33</span>
                                </div>
                            </div>
                        </div>
                    </div>
                    <div class="tab-bar">
                        <div class="tab-item">
                            <i class="fas fa-home tab-icon"></i>
                            <span class="tab-label">主页</span>
                        </div>
                        <div class="tab-item">
                            <i class="fas fa-tree tab-icon"></i>
                            <span class="tab-label">3D果林</span>
                        </div>
                        <div class="tab-item active">
                            <i class="fas fa-graduation-cap tab-icon"></i>
                            <span class="tab-label">果林学堂</span>
                        </div>
                        <div class="tab-item">
                            <i class="fas fa-user tab-icon"></i>
                            <span class="tab-label">我的</span>
                        </div>
                    </div>
                </div>
            </div>
        </div>

        <!-- 客服咨询界面 -->
        <div id="service" class="prototype-tab">
            <div class="iphone-frame">
                <div class="screen">
                    <div class="status-bar">
                        <span>9:41</span>
                        <div class="flex space-x-2">
                            <i class="fas fa-signal"></i>
                            <i class="fas fa-wifi"></i>
                            <i class="fas fa-battery-full"></i>
                        </div>
                    </div>
                    <div class="p-4 pb-24">
                        <!-- 常见问题 -->
                        <div class="bg-white rounded-xl shadow-sm p-4 mb-4">
                            <h2 class="text-lg font-semibold text-gray-800 mb-4">常见问题</h2>
                            <div class="space-y-3">
                                <div class="flex items-center justify-between p-3 bg-gray-50 rounded-lg">
                                    <span class="text-gray-800">如何连接无人机？</span>
                                    <i class="fas fa-chevron-right text-gray-400"></i>
                                </div>
                                <div class="flex items-center justify-between p-3 bg-gray-50 rounded-lg">
                                    <span class="text-gray-800">如何查看飞行记录？</span>
                                    <i class="fas fa-chevron-right text-gray-400"></i>
                                </div>
                                <div class="flex items-center justify-between p-3 bg-gray-50 rounded-lg">
                                    <span class="text-gray-800">如何导出监测数据？</span>
                                    <i class="fas fa-chevron-right text-gray-400"></i>
                                </div>
                            </div>
                        </div>

                        <!-- 聊天记录 -->
                        <div class="space-y-4">
                            <!-- 客服消息 -->
                            <div class="flex items-start space-x-2">
                                <div class="w-8 h-8 rounded-full bg-green-100 flex items-center justify-center">
                                    <i class="fas fa-headset text-green-600"></i>
                                </div>
                                <div class="chat-bubble service">
                                    <p class="text-gray-800">您好！我是智能果林监测App的客服，请问有什么可以帮到您？</p>
                                    <span class="text-xs text-gray-500 mt-1 block">10:30</span>
                                </div>
                            </div>

                            <!-- 用户消息 -->
                            <div class="flex items-start justify-end space-x-2">
                                <div class="chat-bubble user">
                                    <p class="text-gray-800">我的无人机连接不上App了，怎么办？</p>
                                    <span class="text-xs text-gray-500 mt-1 block">10:32</span>
                                </div>
                            </div>

                            <!-- 客服消息 -->
                            <div class="flex items-start space-x-2">
                                <div class="w-8 h-8 rounded-full bg-green-100 flex items-center justify-center">
                                    <i class="fas fa-headset text-green-600"></i>
                                </div>
                                <div class="chat-bubble service">
                                    <p class="text-gray-800">请您按照以下步骤尝试重新连接：</p>
                                    <ol class="list-decimal pl-5 mt-2 text-gray-800">
                                        <li>确保无人机和手机都已开启蓝牙</li>
                                        <li>重启App和无人机</li>
                                        <li>在App设置中清除设备缓存</li>
                                        <li>重新扫描并连接设备</li>
                                    </ol>
                                    <p class="text-gray-800 mt-2">如果问题仍然存在，您可以尝试更新App或联系我们的技术支持团队。</p>
                                    <span class="text-xs text-gray-500 mt-1 block">10:33</span>
                                </div>
                            </div>
                        </div>
                    </div>
                    <div class="tab-bar">
                        <div class="tab-item">
                            <i class="fas fa-home tab-icon"></i>
                            <span class="tab-label">主页</span>
                        </div>
                        <div class="tab-item">
                            <i class="fas fa-tree tab-icon"></i>
                            <span class="tab-label">3D果林</span>
                        </div>
                        <div class="tab-item active">
                            <i class="fas fa-graduation-cap tab-icon"></i>
                            <span class="tab-label">果林学堂</span>
                        </div>
                        <div class="tab-item">
                            <i class="fas fa-user tab-icon"></i>
                            <span class="tab-label">我的</span>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>

    <script>
        function showTab(tabId) {
            // 隐藏所有标签页
            document.querySelectorAll('.prototype-tab').forEach(tab => {
                tab.classList.remove('active');
            });
            
            // 显示选中的标签页
            document.getElementById(tabId).classList.add('active');
            
            // 更新标签按钮状态
            document.querySelectorAll('.tab-button').forEach(button => {
                button.classList.remove('active');
            });
            event.target.classList.add('active');
        }
    </script>
</body>
</html> 
