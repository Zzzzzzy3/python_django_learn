![[Pasted image 20250709100200.png]]
paginator 
```html
<!-- 在菜品表格下方添加这个分页导航 -->
<div class="card-footer">
    <nav aria-label="Dish pagination">
        <ul class="pagination justify-content-center">
            {% if page_obj.has_previous %}
            <li class="page-item">
                <a class="page-link" href="?page=1" aria-label="First">
                    &laquo;&laquo;
                </a>
            </li>
            <li class="page-item">
                <a class="page-link" href="?page={{ page_obj.previous_page_number }}" aria-label="Previous">
                    &laquo;
                </a>
            </li>
            {% endif %}
            
            {% for num in page_obj.paginator.page_range %}
                {% if page_obj.number == num %}
                <li class="page-item active"><a class="page-link" href="?page={{ num }}">{{ num }}</a></li>
                {% elif num > page_obj.number|add:'-3' and num < page_obj.number|add:'3' %}
                <li class="page-item"><a class="page-link" href="?page={{ num }}">{{ num }}</a></li>
                {% endif %}
            {% endfor %}
            
            {% if page_obj.has_next %}
            <li class="page-item">
                <a class="page-link" href="?page={{ page_obj.next_page_number }}" aria-label="Next">
                    &raquo;
                </a>
            </li>
            <li class="page-item">
                <a class="page-link" href="?page={{ page_obj.paginator.num_pages }}" aria-label="Last">
                    &raquo;&raquo;
                </a>
            </li>
            {% endif %}
        </ul>
    </nav>
    <div class="text-center text-muted">
        显示 {{ page_obj.start_index }} 到 {{ page_obj.end_index }} 条菜品，共 {{ page_obj.paginator.count }} 条
    </div>
</div>
```
显然会刷新页面

## 2.实现分页导航点击时，仅通过 AJAX 异步请求更新菜品表格部分，不刷新整页。
