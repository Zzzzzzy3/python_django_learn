```css
body {  
    font-family: 'Segoe UI', system-ui, sans-serif;  
    background: #f4f6fa;  
    overflow-x: hidden;  
    /*取消仪表的col-lg-9*/  
  
}  
  
  
.sidebar {  
    background: #ffffff;  
    box-shadow: 2px 0 8px rgba(0, 0, 0, 0.05);  
    transition: all 0.3s;  
}  
  
.list-group-item {  
    border: none;  
    margin: 4px 0;  
    line-height: 2.4;  
    border-radius: 8px !important;  
    transition: all 0.2s;  
}  
  
.list-group-item.active {  
    background: linear-gradient(135deg, #6366f1, #818cf8) !important;  
    box-shadow: 0 4px 12px rgba(99, 102, 241, 0.2);  
    transform: translateX(8px);  
}  
  
.list-group-item:not(.active):hover {  
    background: rgba(99, 102, 241, 0.06);  
    transform: translateX(4px);  
}  
  
.list-group-item {  
    transition: all 0.25s cubic-bezier(0.4, 0, 0.2, 1);  
}  
  
.navbar {  
    background: linear-gradient(135deg, #6366f1, #4f46e5) !important;  
    box-shadow: 0 2px 8px rgba(0, 0, 0, 0.1);  
    border-bottom: 1px solid rgba(255, 255, 255, 0.1);  
}  
  
.card {  
    border: none;  
    border-radius: 12px;  
    background: linear-gradient(145deg, rgba(255, 255, 255, 0.95), rgba(248, 249, 250, 0.95));  
    box-shadow: 0 1px 2px rgba(0, 0, 0, 0.05),  
    0 8px 24px -6px rgba(99, 102, 241, 0.15);  
    transition: all 0.4s cubic-bezier(0.23, 1, 0.32, 1);  
    overflow: hidden;  
    position: relative;  
    border: 1px solid rgba(255, 255, 255, 0.3);  
}  
  
.card::after {  
    content: '';  
    position: absolute;  
    bottom: 0;  
    left: 0;  
    right: 0;  
    height: 4px;  
    background: linear-gradient(90deg,  
    rgba(99, 102, 241, 0.4) 0%,  
    rgba(165, 180, 252, 0.3) 50%,  
    rgba(99, 102, 241, 0.4) 100%);  
    opacity: 0.6;  
    transition: opacity 0.3s ease;  
}  
  
.card:hover {  
    transform: translateY(-6px) scale(1.02);  
    box-shadow: 0 12px 32px -8px rgba(99, 102, 241, 0.25),  
    0 4px 24px -6px rgba(16, 185, 129, 0.15);  
}  
  
.card:hover::after {  
    opacity: 1;  
}  
  
/* 新增卡片图片样式 */.card-img {  
    width: 100%;  
    height: 180px;  
    object-fit: cover;  
    border-radius: 12px 12px 0 0;  
    transition: transform 0.3s ease;  
}  
  
.card:hover .card-img {  
    transform: scale(1.05);  
}  
  
/* 徽章样式 */.badge-gradient-success {  
    background: linear-gradient(135deg, rgba(16, 185, 129, 0.9), rgba(5, 150, 105, 0.95));  
    color: white !important;  
    box-shadow: 0 2px 8px -2px rgba(16, 185, 129, 0.3);  
    border: 1px solid rgba(255, 255, 255, 0.15);  
    border-radius: 8px;  
    font-weight: 500;  
    padding: 6px 12px;  
}  
  
.badge-gradient-warning {  
    background: linear-gradient(135deg, rgba(245, 158, 11, 0.9), rgba(217, 119, 6, 0.95));  
    color: white !important;  
    box-shadow: 0 2px 8px -2px rgba(245, 158, 11, 0.3);  
    border: 1px solid rgba(255, 255, 255, 0.15);  
    border-radius: 8px;  
    font-weight: 500;  
    padding: 6px 12px;  
}  
  
.badge-gradient-danger {  
    background: linear-gradient(135deg, rgba(239, 68, 68, 0.9), rgba(185, 28, 28, 0.95));  
    color: white !important;  
    box-shadow: 0 2px 8px -2px rgba(239, 68, 68, 0.3);  
    border: 1px solid rgba(255, 255, 255, 0.15);  
    border-radius: 8px;  
    font-weight: 500;  
    padding: 6px 12px;  
}  
  
.badge-gradient-success:hover,  
.badge-gradient-warning:hover,  
.badge-gradient-danger:hover {  
    transform: translateY(-1px);  
    box-shadow: 0 4px 12px -2px rgba(99, 102, 241, 0.3);  
    transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);  
}  
  
/* 表格样式 */.table {  
    --bs-table-bg: transparent;  
}  
  
.table-hover > tbody > tr:hover {  
    --bs-table-accent-bg: rgba(99, 102, 241, 0.04);  
    transform: scale(1.002);  
}  
  
.table-striped > tbody > tr:nth-child(odd) > td {  
    background-color: rgba(249, 250, 251, 0.6);  
}  
  
.table th {  
    background: linear-gradient(180deg, #f8f9fa, #f1f3f5);  
    font-weight: 600;  
    color: #374151;  
}  
  
/* 图表容器 */#dataChart {  
    min-height: 400px;  
}  
  
  
/* 侧边栏 */.sidebar {  
    height: 100vh;  
    background: #f8f9fa;  
    position: fixed;  
    width: 280px;  
}  
  
.main-content {  
    margin-left: 280px;  
    padding: 20px;  
}  
  
@media (max-width: 768px) {  
    .sidebar {  
        width: 100%;  
        position: relative;  
        height: auto;  
    }  
  
    .main-content {  
        margin-left: 0;  
    }  
}  
  
#dashboard .col-lg-9 {  
    width: auto !important; /* 取消固定宽度 */    flex: 0 0 auto !important; /* 取消 flex 布局的固定比例 */}  
  
/* 箭头连接样式 */.animated-arrow {  
    width: 60px;  
    height: 2px;  
    background: #0d6efd;  
    position: relative;  
    animation: arrow-pulse 1.5s infinite;  
}  
  
.animated-arrow::after {  
    content: '';  
    position: absolute;  
    right: -8px;  
    top: -6px;  
    width: 15px;  
    height: 15px;  
    border-right: 3px solid #0d6efd;  
    border-top: 3px solid #0d6efd;  
    transform: rotate(45deg);  
}  
  
@keyframes arrow-pulse {  
    0% {  
        width: 60px;  
        opacity: 0.8;  
    }  
    50% {  
        width: 80px;  
        opacity: 1;  
    }  
    100% {  
        width: 60px;  
        opacity: 0.8;  
    }  
}  
  
/* 响应式调整 */@media (max-width: 768px) {  
    .arrow-container {  
        display: none;  
    }  
  
    .col-md-1 {  
        display: none;  
    }  
}  
/* 垂直箭头样式 */.vertical-arrow {  
    height: 60px;  
    width: 2px;  
    background: #0d6efd;  
    position: relative;  
    animation: arrow-vertical-pulse 1.5s infinite;  
    margin: 20px 0;  
}  
  
.vertical-arrow::after {  
    content: '';  
    position: absolute;  
    bottom: -8px;  
    left: 50%;  
    width: 15px;  
    height: 15px;  
    border-right: 3px solid #0d6efd;  
    border-top: 3px solid #0d6efd;  
    transform: rotate(135deg);  
    margin-left: -7px; /* 微调居中位置 */}  
  
@keyframes arrow-vertical-pulse {  
    0% { height: 60px; opacity: 0.8; }  
    50% { height: 80px; opacity: 1; }  
    100% { height: 60px; opacity: 0.8; }  
}
```