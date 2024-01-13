Тестовое задание - https://docs.google.com/document/d/1Ld4I-W06glavKmzVfUudqQXNHNEcdrcvR4TLDwll434/edit?usp=sharing 

Компанент расположен в /local/components/test/

Страница для проверки доступна по ссылке - https://odejda.reinero.ru/test-task1/ .

При первом заходе на странице отображаются кешированные данные, данные обновляются каждые три минуты. 
Если нажать кнопку обновить, страница перезагрузится через ajax с новым некешируемым запросом. 
При повторном обновлении отобразятся кешированные данные с первого запроса если не прошло, три минуты.

Сам компонент вызван на странице через код - 
```php
<?
$APPLICATION->IncludeComponent(
	"test:test1.comp",
	".default",
	array(
		"COMPONENT_TEMPLATE" => ".default",
		"SET_TITLE_BROWSER" => "Y",
		"IBLOCK_TYPE" => "directories",
		"IBLOCK_ID" => "4",
		"VIEW_RULE" => "0",
		"FIELDS" => "NAME, ID",
		"AJAX_MODE" => "Y",
		"CACHE_TIME" => "180",
		"CACHE_GROUPS" => "N",
		"CACHE_TYPE" => "A",
		
	),
	false
);
?>
```
