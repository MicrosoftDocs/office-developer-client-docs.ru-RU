---
title: New in Visio for developers
manager: soliver
ms.date: 09/18/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 7e3fb858-0ab8-bd2e-217c-c85b10d79785
description: В этом документе представлены чертах расширения и дополнения для разработчиков в Visio 2013. Для разработчиков, все готово для запуска перехода на платформу она предоставляет достаточно сведений для начала создания кода для Visio 2013.
ms.openlocfilehash: 3e0f119ac0b6b43737ff394a4553405982a4ec04
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814305"
---
# <a name="new-in-visio-for-developers"></a>New in Visio for developers

В этом документе представлены чертах расширения и дополнения для разработчиков в Visio 2013. Для разработчиков, все готово для запуска перехода на платформу она предоставляет достаточно сведений для начала создания кода для Visio 2013.
  
## <a name="introduction"></a>Введение
<a name="vis15_WhatsNew_Intro"> </a>

Visio 2013 предоставляет мощные платформа для пользовательских решений рисунка. Новые объекты, семейства сайтов, свойства, методы, перечисления и событий, а также новые ячейки таблицы свойств фигуры и функции, предоставляют больше возможностей для определения поведения элементов в решениях.
  
Новые возможности интерес для разработчиков в Visio 2013 являются новый формат файла; Надежная обновления тем; Изменение компонента фигуры (позволяя замените фигур); новые эффекты фигур; улучшения комментирование; совместное редактирование в SharePoint Server 2013; настраиваемое кадрирование изображений; относительное геометрия; Поддержка для данных Business Connectivity Services (BCS); обновления в службах Visio в Microsoft SharePoint Server 2013; и его компонентов дубликата страницы. В этом разделе дает краткое описание каждого из этих функций и упоминаются некоторые новые Visio объекты и члены, которые связаны с возможностями и отображен в Visual Basic для приложений (VBA). Для получения сведений об этих возможностях и соответствующие образцы кода см в [Центр разработчиков Visio](http://msdn.microsoft.com/en-us/office/aa905478.aspx).
  
> [!NOTE]
> Visio 2013 включает в себя многие новые ShapeSheet ячеек, строк и функции для поддержки новых функций в Visio. Дополнительные сведения о новые возможности в таблице свойств фигуры Visio 2013 в статье [возможности впервые для разработчиков таблиц свойств фигур Visio](what-s-new-for-visio-shapesheet-developers.md). 
  
## <a name="new-file-format"></a>Новый формат файла
<a name="vis15_WhatsNew_NewFF"> </a>

Visio 2013 включает новый формат файла, основанный на стандарте Open Packaging Conventions (OPC) (ISO 29500, часть 2), и XML-элементы из предыдущего формата файла Visio XML (VDX). Это формат ZIP-файл на основе XML, аналогичную форматы файлов, используемые в других приложениях.
  
Новый формат файла поддерживается в Visio 2013 и Visio в Microsoft SharePoint Server 2013, можно сохранить документа непосредственно в библиотеку SharePoint Server без необходимости опубликуйте файл как Visio Web рисунка (.vdw) Visio. Тем не менее служб Visio возможность чтения и отображение файлов веб-документа Visio.
  
Новый формат файла включает в себя следующие типы файлов (с расширением):
  
- VSDX (документ Visio),
    
- VSDM (документ Visio с поддержкой макросов),
    
- VSSX (набор элементов Visio),
    
- VSSM (набор элементов Visio с поддержкой макросов),
    
- VSTX (шаблон Visio),
    
- VSTM (шаблон Visio с поддержкой макросов).
    
Используя существующую поддержку чтения и записи в пакет форматов файлов (например, [System.IO.Packaging](https://msdn.microsoft.com/library/System.IO.Packaging.aspx) ) и анализа XML ( [System.Xml.Linq](https://msdn.microsoft.com/library/System.Xml.Linq.aspx) ), можно программно обрабатывать новые форматы файлов. 
  
Visio 2013 сохраняет возможность чтения старые форматы файлов (.vsd, .vss, .vst, .vdx, .vsx, .vtx, .vdw, .vwi). Visio 2013 не сохраняет предыдущих формат файлов Visio в формате XML (.vdx). Решения или средства, которые используют предыдущие Visio XML-файл формата (.vdx) файлы может потребоваться оптимизации для чтения в новый формат файла и его схемы.
  
Службы Visio сохраняет возможность отображения в формат веб-документа Visio (.vdw) в браузере. Он теперь также выводит нового Visio документа (vsdx (en) и Visio макросами рисунка (.vsdm) форматы.
  
## <a name="themes"></a>Темы
<a name="vis15_WhatsNew_Themes"> </a>

В Visio 2013 темы изменены: расширен набор эффектов и стилей, включая интеграцию эффектов коллекций фигур. Пользователи могут теперь определиться всеобъемлющая стилей с помощью схемы индивидуальной настройки схемы с их вариантов и выделите отдельные фигуры с экспресс-стилей. Разработчиков таблиц свойств фигур можно воспользоваться преимуществами этих функций с помощью новых функций и ячеек в таблице свойств фигуры.
  
Можно управлять тем на уровне объекта [страницы](http://msdn.microsoft.com/library/7a7f37ab-b448-eb70-b4f1-c185dfbd511e%28Office.15%29.aspx), [фигуры](http://msdn.microsoft.com/library/da7a8872-4ebb-a607-e0ed-eebf68ff5630%28Office.15%29.aspx)и [Выделение](http://msdn.microsoft.com/library/e5734140-6dbe-7de8-9695-1a22fb4ac628%28Office.15%29.aspx) . Новые интерфейсы API для работы с тем включают метод [Page.SetTheme](http://msdn.microsoft.com/library/5a186f58-9a7a-bd8a-826b-85da75a4d59f%28Office.15%29.aspx) , метод [Page.SetThemeVariant](http://msdn.microsoft.com/library/8393a95f-83ca-0efa-d987-ae498bfe5e9d%28Office.15%29.aspx) , метод [Shape.SetQuickStyle](http://msdn.microsoft.com/library/aebe80cb-fae9-0be7-e903-882f6eb58b63%28Office.15%29.aspx) и метод [Selection.SetQuickStyle](http://msdn.microsoft.com/library/39b810b5-0738-daed-0103-8a2df07559c6%28Office.15%29.aspx) . 
  
Подробный список функций новые интерфейсы API в Visio 2013 см в разделе [изменения в объектной модели Visio](#vis15_WhatsNew_NewOM) в этой статье. Дополнительные сведения о новой ячейки таблицы свойств фигуры в Visio 2013 в статье [возможности впервые для разработчиков таблиц свойств фигур Visio](what-s-new-for-visio-shapesheet-developers.md).
  
## <a name="change-shape"></a>Изменение фигур
<a name="vis15_WhatsNew_ChangeShapes"> </a>

Visio 2013 включает в себя фигуры замены API, которое позволяет вам для замены одного или нескольких фигур другую фигуру, содержащихся в набор элементов, сохраняя некоторые из локальных значений из исходной формы, как фигура фигурой текст, данные фигуры или форматирование фигур. Фигура разработчики могут обновите параметры таблицы свойств фигуры свои собственные фигуры для указания режима изменения фигуры для их формы. Новые интерфейсы API позволяют [Shape.ReplaceShapes](http://msdn.microsoft.com/library/b330a63d-4e3f-0c4d-c38c-6ee806670225%28Office.15%29.aspx) и [Selection.ReplaceShapes](http://msdn.microsoft.com/library/dc278901-77ce-e1fe-c44f-f464bbb1c360%28Office.15%29.aspx) методы и события [ReplaceShape](http://msdn.microsoft.com/library/26c4e7cb-6618-6d2f-a4be-515584f8cd10%28Office.15%29.aspx) . 
  
Подробный список функций новые интерфейсы API в Visio 2013 см в разделе [изменения в объектной модели Visio](#vis15_WhatsNew_NewOM) в этой статье. Дополнительные сведения о новой ячейки таблицы свойств фигуры в Visio 2013 в статье [возможности впервые для разработчиков таблиц свойств фигур Visio](what-s-new-for-visio-shapesheet-developers.md).
  
## <a name="shape-effects"></a>Эффекты фигур
<a name="vis15_WhatsNew_ShapeEffects"> </a>

Новые эффекты фигур, такие как багетная рамка, трехмерное вращение, свечение, отражение и эскизы, были добавлены в Visio 2013. Таблицы свойств фигуры включает в себя новые ячейки для работы с этим влияет на.
  
Дополнительные сведения о новой ячейки таблицы свойств фигуры в Visio 2013 в статье [возможности впервые для разработчиков таблиц свойств фигур Visio](what-s-new-for-visio-shapesheet-developers.md).
  
## <a name="commenting"></a>Комментарии
<a name="vis15_WhatsNew_Commenting"> </a>

Visio 2013 включает новую структуру создания комментариев. Комментарии теперь можно связывать с конкретными фигурами или страницами. Visio 2013 включает в себя две новые объекты, [комментарии](http://msdn.microsoft.com/library/f028cc03-0ef1-8017-a936-d30d45211864%28Office.15%29.aspx) и [комментарии](http://msdn.microsoft.com/library/7cd0ee53-6b8d-a03b-ecd6-f6f6dda0f2d4%28Office.15%29.aspx). Новые интерфейсы API для программного доступа к комментарии включать свойства, [Document.Comments](http://msdn.microsoft.com/library/15a322ad-70eb-1487-701d-76e2fde73309%28Office.15%29.aspx), [Page.Comments](http://msdn.microsoft.com/library/9618c86c-96c0-be95-ee20-5d1b99f4d5e8%28Office.15%29.aspx), [Shape.Comments](http://msdn.microsoft.com/library/498eca91-beb9-b764-0262-a935e5205710%28Office.15%29.aspx)и [Page.ShapeComments](http://msdn.microsoft.com/library/b7d86594-ba1f-627b-222f-905da1b1201e%28Office.15%29.aspx) . 
  
Visio Services включает в себя интерфейсы API JavaScript для чтения комментариев из страницы или фигуры на схеме.
  
Подробный список функций новые интерфейсы API в Visio 2013 см в разделе [изменения в объектной модели Visio](#vis15_WhatsNew_NewOM) в этой статье. 
  
> [!NOTE]
> Комментарии становятся недоступными по таблице свойств фигуры. 
  
## <a name="coauthoring"></a>Совместное редактирование
<a name="vis15_WhatsNew_Coauthoring"> </a>

Visio 2013 включает в себя возможность совместно редактировать схемы, сохраненные в SharePoint или Microsoft OneDrive. Разработчики имеют доступ к [Document.AfterDocumentMerge](http://msdn.microsoft.com/library/50658da5-592a-4d16-908f-c6abe3050f09%28Office.15%29.aspx) событие, которое содержит сведения об изменениях схемы из-за совместного редактирования. Разработчики решений также имеют возможность отключить совместное редактирование в соответствии с их настраиваемых требованиям, с помощью [NoCoauth](nocoauth-cell-document-properties-section.md) ячеек в таблице свойств фигуры документа. 
  
Подробный список функций новые интерфейсы API в Visio 2013 см в разделе [изменения в объектной модели Visio](#vis15_WhatsNew_NewOM) в этой статье. 
  
## <a name="customizable-image-clipping"></a>Настраиваемое кадрирование изображений
<a name="vis15_WhatsNew_ClipImages"> </a>

Visio 2013 поддерживает задание настраиваемого контура кадрирования изображения, который позволяет обрезать изображения до любой формы. Это расширяет емкость Visio 2010, которые поддерживаются изображения Вырезка прямоугольный образом. Эта функция доступна в таблице свойств фигуры с помощью [ClippingPath](clippingpath-cell-foreign-image-info-section.md) ячейки в раздел **внешнего рисунка** . 
  
Дополнительные сведения о новой ячейки таблицы свойств фигуры в Visio 2013 в статье [возможности впервые для разработчиков таблиц свойств фигур Visio](what-s-new-for-visio-shapesheet-developers.md).
  
## <a name="relative-geometries"></a>Относительная геометрия
<a name="vis15_WhatsNew_RelativeGeometry"> </a>

В предыдущих версиях программы Геометрия фигуры определен с помощью формул, которые зависят от значения высоты и ширины фигуры. Например в Visio 2010 грани множество встроенных фигур Visio были определены путем умножения значения высоты и ширины фигуры на константу. Эти фигуры имелся в разделах **геометрии** , в которых использовался [MoveTo](moveto-row-geometry-section.md) или [LineTo](lineto-row-geometry-section.md) строк (например) с формулами, как `Width*1` и `Height*0`.
  
Visio 2013 теперь поддерживает относительную геометрию в таблице свойств фигуры. Относительная геометрия теперь могут использоваться разработчиками фигуры для указания геометрия как простой значений или формул, которые умножить значения высоты и ширины автоматически. Вершины фигуры можно теперь выразить константы, например, устраняя необходимость express вершины как проводите несколько фигуры ширину или высоту. Он облегчает для разработчиков для создания фигур, с помощью улучшения производительности и размер. Новые строки включает строки [RelMoveTo](relmoveto-row-geometry-section.md) и [RelLineTo](rellineto-row-geometry-section.md) , где **X** и **Y** значений ячеек, автоматически умножаются ширину или высоту фигуры (соответственно). 
  
Дополнительные сведения о новых строк таблицы свойств фигуры в Visio 2013 в статье [возможности впервые для разработчиков таблиц свойств фигур Visio](what-s-new-for-visio-shapesheet-developers.md).
  
## <a name="support-for-business-connectivity-services-bcs-data"></a>Поддержка данных Business Connectivity Services (BCS)
<a name="vis15_WhatsNew_BCS"> </a>

Схемы Visio 2013 теперь могут быть подключены к внешним спискам на серверах SharePoint Server 2013. Внешний список является источником контента внешними по отношению к SharePoint (например, таблицы SQL Server), который был подключен к списку SharePoint с помощью Microsoft Business Connectivity Services (BCS). Службы Visio поддерживают возможность обновления схемы Visio как обновления данных.
  
Дополнительные сведения о новые возможности служб Visio в статье [Служб Visio в SharePoint 2013](http://msdn.microsoft.com/en-us/library/jj164027%28office.15%29.aspx). Дополнительные сведения о Business Connectivity Services (BCS) можно [Business Connectivity Services в SharePoint 2013](http://msdn.microsoft.com/en-us/library/jj163782%28office.15%29.aspx).
  
## <a name="improvements-in-visio-services"></a>Усовершенствования в службах Visio
<a name="vis15_WhatsNew_VisioServices"> </a>

Службы Visio в Microsoft SharePoint Server 2013 включает в себя множество усовершенствований. Как уже было сказано ранее, службы Visio поддерживают новый формат файла Visio (vsdx (en) и .vsdm). Обновление данных и пересчет, включая возможность пересчет формул по всей схемы расширил служб Visio. 
  
Дополнительные сведения о новые возможности служб Visio в статье [Служб Visio в SharePoint 2013](http://msdn.microsoft.com/en-us/library/jj164027%28office.15%29.aspx).
  
## <a name="duplicate-page"></a>Дублирование страницы
<a name="vis15_WhatsNew_DuplicatePage"> </a>

Теперь можно скопировать страницы и всех его фигур в пределах того же документа в Visio 2013. Соответственно объект **Page** имеет новый метод, [дублирующиеся](http://msdn.microsoft.com/library/394be23b-997d-0da1-b3bd-8278564fb4e0%28Office.15%29.aspx), которое дублирует страницы и возвращает объект новой **страницы** . 
  
## <a name="visio-object-model-changes"></a>Изменения в объектной модели Visio
<a name="vis15_WhatsNew_NewOM"> </a>

Новые объекты, свойства, методы и события были добавлены к объектной модели Visio для обеспечения поддержки программирования для новых функций Visio 2013. Кроме того улучшения объектной модели устранения часто используемые для разработчиков-запросов для изменения платформу.
  
### <a name="new-members"></a>Новые элементы

Существующие объекты в объектной модели Visio были добавлены следующие члены.
  
 **В таблице 1. Расширения объектной модели Visio**
  
|**Объект или семейства сайтов**|**Новые элементы**|
|:-----|:-----|
|[Объект Application (Visio)](http://msdn.microsoft.com/library/5b3c8939-793f-116f-11b8-1d4170d95a63%28Office.15%29.aspx) <br/> |[Событие Application.AfterReplaceShapes (Visio)](http://msdn.microsoft.com/library/b02de031-086a-41cc-d832-5434b8096444%28Office.15%29.aspx) <br/> |
||[Событие Application.BeforeReplaceShapes (Visio)](http://msdn.microsoft.com/library/fbf44569-0539-9292-ce20-1f9e34238b33%28Office.15%29.aspx) <br/> |
||[Событие Application.QueryCancelReplaceShapes (Visio)](http://msdn.microsoft.com/library/50c0f2a6-f534-f3af-7e83-c865abda8bf9%28Office.15%29.aspx) <br/> |
||[Событие Application.ReplaceShapesCanceled (Visio)](http://msdn.microsoft.com/library/e8eecd64-e4bd-d2c4-b942-c5ff607a4121%28Office.15%29.aspx) <br/> |
|[Объект ApplicationSettings (Visio)](http://msdn.microsoft.com/library/f2e24211-ecc6-e0f5-4c00-fc50f98a3505%28Office.15%29.aspx) <br/> |[Свойство ApplicationSettings.EnterCommitsText (Visio)](http://msdn.microsoft.com/library/ba9ce9fa-d224-cdc3-668d-46c1849911c7%28Office.15%29.aspx) <br/> |
||[Свойство ApplicationSettings.SVGExportFormat (Visio)](http://msdn.microsoft.com/library/9e7ca1cb-5ace-b75b-0e59-61566b9a0169%28Office.15%29.aspx) <br/> |
|[Объект Document (Visio)](http://msdn.microsoft.com/library/21640062-13a2-a2b2-7c61-7e707671207c%28Office.15%29.aspx) <br/> |[Событие Document.AfterDocumentMerge (Visio)](http://msdn.microsoft.com/library/50658da5-592a-4d16-908f-c6abe3050f09%28Office.15%29.aspx) <br/> |
||[Свойство Document.Comments (Visio)](http://msdn.microsoft.com/library/15a322ad-70eb-1487-701d-76e2fde73309%28Office.15%29.aspx) <br/> |
||[Свойство Document.CompatibilityMode (Visio)](http://msdn.microsoft.com/library/98fc00d3-5d2b-218e-9828-b5581ee7313d%28Office.15%29.aspx) <br/> |
|[Объект документы (Visio)](http://msdn.microsoft.com/library/e9291149-964e-c6fb-4c62-bf2f35a6a0a7%28Office.15%29.aspx) <br/> |[Событие Documents.AfterDocumentMerge (Visio)](http://msdn.microsoft.com/library/cac0544d-77b9-b722-cfdb-e42475ce2558%28Office.15%29.aspx) <br/> |
||[Событие Documents.AfterReplaceShapes (Visio)](http://msdn.microsoft.com/library/e01c069e-440b-7b8b-8d7d-cdb664f6e2d6%28Office.15%29.aspx) <br/> |
||[Событие Documents.BeforeReplaceShapes (Visio)](http://msdn.microsoft.com/library/55a66c47-a2ca-5c8a-2693-aaa1b079c704%28Office.15%29.aspx) <br/> |
||[Событие Documents.QueryCancelReplaceShapes (Visio)](http://msdn.microsoft.com/library/d613730e-04c8-d17f-0ad1-19e976aa107d%28Office.15%29.aspx) <br/> |
||[Событие Documents.ReplaceShapesCanceled (Visio)](http://msdn.microsoft.com/library/94a20fe7-da09-4e3c-d048-05ba0b8f1070%28Office.15%29.aspx) <br/> |
|[Объект InvisibleApp (Visio)](http://msdn.microsoft.com/library/70a30571-2017-af8b-eaa1-bf93c758a46a%28Office.15%29.aspx) <br/> |[Событие InvisibleApp.AfterReplaceShapes (Visio)](http://msdn.microsoft.com/library/5d7b8ec2-ef65-1a49-fb50-3fae95d56761%28Office.15%29.aspx) <br/> |
||[Событие InvisibleApp.BeforeReplaceShapes (Visio)](http://msdn.microsoft.com/library/bd0e37ca-887a-4d53-3b0c-3339492df3dd%28Office.15%29.aspx) <br/> |
||[Событие InvisibleApp.QueryCancelReplaceShapes (Visio)](http://msdn.microsoft.com/library/5e5d9b76-dfd4-1d02-d205-9e64350449d5%28Office.15%29.aspx) <br/> |
||[Событие InvisibleApp.ReplaceShapesCanceled (Visio)](http://msdn.microsoft.com/library/17e43497-c7a8-8546-595c-4630afb301a3%28Office.15%29.aspx) <br/> |
|[Объект Page (Visio)](http://msdn.microsoft.com/library/7a7f37ab-b448-eb70-b4f1-c185dfbd511e%28Office.15%29.aspx) <br/> |[Событие Page.AfterReplaceShapes (Visio)](http://msdn.microsoft.com/library/e4005987-acb1-78d7-91fb-c3c2d5b036e3%28Office.15%29.aspx) <br/> |
||[Событие Page.BeforeReplaceShapes (Visio)](http://msdn.microsoft.com/library/57ea9836-74dd-77c2-6541-f8f61b89c0b6%28Office.15%29.aspx) <br/> |
||[Свойство Page.Comments (Visio)](http://msdn.microsoft.com/library/9618c86c-96c0-be95-ee20-5d1b99f4d5e8%28Office.15%29.aspx) <br/> |
||[Метод Page.Duplicate (Visio)](http://msdn.microsoft.com/library/394be23b-997d-0da1-b3bd-8278564fb4e0%28Office.15%29.aspx) <br/> |
||[Метод Page.GetTheme (Visio)](http://msdn.microsoft.com/library/31c84e69-0bc8-2d1a-84d8-7397110d74ae%28Office.15%29.aspx) <br/> |
||[Метод Page.GetThemeVariant (Visio)](http://msdn.microsoft.com/library/40c2be31-fdb0-68ee-a129-2788b1b17c82%28Office.15%29.aspx) <br/> |
||[Событие Page.QueryCancelReplaceShapes (Visio)](http://msdn.microsoft.com/library/17ead23f-825a-c608-3315-e2eed6784cd5%28Office.15%29.aspx) <br/> |
||[Событие Page.ReplaceShapesCanceled (Visio)](http://msdn.microsoft.com/library/867b1fc1-96bd-cbeb-fd61-b02a96e039ca%28Office.15%29.aspx) <br/> |
||[Метод Page.SetTheme (Visio)](http://msdn.microsoft.com/library/5a186f58-9a7a-bd8a-826b-85da75a4d59f%28Office.15%29.aspx) <br/> |
||[Метод Page.SetThemeVariant (Visio)](http://msdn.microsoft.com/library/8393a95f-83ca-0efa-d987-ae498bfe5e9d%28Office.15%29.aspx) <br/> |
||[Свойство Page.ShapeComments (Visio)](http://msdn.microsoft.com/library/b7d86594-ba1f-627b-222f-905da1b1201e%28Office.15%29.aspx) <br/> |
|[Объект страницы (Visio)](http://msdn.microsoft.com/library/45eec568-b5cc-5e80-ff5c-4dfa567efb5d%28Office.15%29.aspx) <br/> |[Событие Pages.AfterReplaceShapes (Visio)](http://msdn.microsoft.com/library/05c33bdd-e697-d36e-46a8-45705e9ad2c2%28Office.15%29.aspx) <br/> |
||[Событие Pages.BeforeReplaceShapes (Visio)](http://msdn.microsoft.com/library/3f6dbc31-0583-dd67-0432-335d6df7a50c%28Office.15%29.aspx) <br/> |
||[Событие Pages.QueryCancelReplaceShapes (Visio)](http://msdn.microsoft.com/library/d11ff976-0016-da6b-92fb-379baa7e8f94%28Office.15%29.aspx) <br/> |
||[Событие Pages.ReplaceShapesCanceled (Visio)](http://msdn.microsoft.com/library/f0ce8c66-7a15-5f91-8c89-e177bc6671d2%28Office.15%29.aspx) <br/> |
|[Объект Selection (Visio)](http://msdn.microsoft.com/library/e5734140-6dbe-7de8-9695-1a22fb4ac628%28Office.15%29.aspx) <br/> |[Метод Selection.ReplaceShape (Visio)](http://msdn.microsoft.com/library/dc278901-77ce-e1fe-c44f-f464bbb1c360%28Office.15%29.aspx) <br/> |
||[Метод Selection.SetQuickStyle (Visio)](http://msdn.microsoft.com/library/39b810b5-0738-daed-0103-8a2df07559c6%28Office.15%29.aspx) <br/> |
|[Объекта Shape (Visio)](http://msdn.microsoft.com/library/da7a8872-4ebb-a607-e0ed-eebf68ff5630%28Office.15%29.aspx) <br/> |[Метод Shape.ChangePicture (Visio)](http://msdn.microsoft.com/library/9193d802-cebd-2bfd-5f8e-400fac36c1a5%28Office.15%29.aspx) <br/> |
||[Свойство Shape.Comments (Visio)](http://msdn.microsoft.com/library/498eca91-beb9-b764-0262-a935e5205710%28Office.15%29.aspx) <br/> |
||[Метод Shape.ReplaceShape (Visio)](http://msdn.microsoft.com/library/b330a63d-4e3f-0c4d-c38c-6ee806670225%28Office.15%29.aspx) <br/> |
||[Метод Shape.SetQuickStyle (Visio)](http://msdn.microsoft.com/library/aebe80cb-fae9-0be7-e903-882f6eb58b63%28Office.15%29.aspx) <br/> |
   
### <a name="new-objects-and-enumerations"></a>Новые объекты и перечисления

Следующие объекты были добавлены к объектной модели Visio.
  
 **В таблице 2. Расширения объектной модели Visio**
  
|**Объект**|**Свойства**|**Методы**|
|:-----|:-----|:-----|
|[Объект CoauthMergeEvent (Visio)](http://msdn.microsoft.com/library/eb9425cb-0108-4909-e334-9cd51e5b9303%28Office.15%29.aspx) <br/> |[Свойство CoauthMergeEvent.BaseDocument (Visio)](http://msdn.microsoft.com/library/7ec09a85-6f51-685b-0c87-4b9eb3266773%28Office.15%29.aspx) <br/> [Свойство CoauthMergeEvent.DownloadDocument (Visio)](http://msdn.microsoft.com/library/19239540-cd5a-13ea-3b26-282ac3676abd%28Office.15%29.aspx) <br/> [Свойство CoauthMergeEvent.ObjectType (Visio)](http://msdn.microsoft.com/library/01baa0c2-75b7-2713-9732-1e7a8a7b33aa%28Office.15%29.aspx) <br/> [Свойство CoauthMergeEvent.Stat (Visio)](http://msdn.microsoft.com/library/d8a96b8e-36b5-c61f-8cea-76266f7eed39%28Office.15%29.aspx) <br/> [Свойство CoauthMergeEvent.WorkingDocument (Visio)](http://msdn.microsoft.com/library/0f3c4358-0d63-df7f-12fe-7f378bacca86%28Office.15%29.aspx) <br/> |Нет  <br/> |
|[Объект комментария (Visio)](http://msdn.microsoft.com/library/f028cc03-0ef1-8017-a936-d30d45211864%28Office.15%29.aspx) <br/> |[Свойство Comment.AssociatedObject (Visio)](http://msdn.microsoft.com/library/e28eed2e-260e-59c9-9b24-631817fe1ae1%28Office.15%29.aspx) <br/> [Свойство Comment.AuthorInitials (Visio)](http://msdn.microsoft.com/library/abc07100-8c5c-9982-674d-40b58c096816%28Office.15%29.aspx) <br/> [Свойство Comment.AuthorName (Visio)](http://msdn.microsoft.com/library/e1da4db8-7a16-16bf-2a5f-be1ac5372d34%28Office.15%29.aspx) <br/> [Свойство Comment.AuthorSipAddress (Visio)](http://msdn.microsoft.com/library/f8d185a9-91b6-471a-3c0e-ffa8a06b36b3%28Office.15%29.aspx) <br/> [Свойство Comment.AuthorSMTPAddress (Visio)](http://msdn.microsoft.com/library/22e04ccc-c524-ca08-d5e2-db68fdb3afb6%28Office.15%29.aspx) <br/> [Свойство Comment.Collapsed (Visio)](http://msdn.microsoft.com/library/9552e379-e351-78d7-e0ed-4f524c3273a1%28Office.15%29.aspx) <br/> [Свойство Comment.CreateDate (Visio)](http://msdn.microsoft.com/library/b643e13e-da12-a992-3a59-99b37f003fb9%28Office.15%29.aspx) <br/> [Свойство Comment.Document (Visio)](http://msdn.microsoft.com/library/d57b1377-b895-1fe1-2f98-ef000fdd9c39%28Office.15%29.aspx) <br/> [Свойство Comment.EditDate (Visio)](http://msdn.microsoft.com/library/4ad13f54-215e-3680-5de6-13715e309fbf%28Office.15%29.aspx) <br/> [Свойство Comment.ObjectType (Visio)](http://msdn.microsoft.com/library/bf0d786d-e1b6-65f1-3112-5dfd4ff324e9%28Office.15%29.aspx) <br/> [Свойство Comment.Stat (Visio)](http://msdn.microsoft.com/library/f457598c-af42-cb83-ecd2-4fd42898ea16%28Office.15%29.aspx) <br/> [Свойство Comment.Text (Visio)](http://msdn.microsoft.com/library/3ec63034-de5f-d9f2-16a5-e06a56883867%28Office.15%29.aspx) <br/> |[Метод Comment.Delete (Visio)](http://msdn.microsoft.com/library/7762f264-f680-5758-7c35-dfe9067b61ca%28Office.15%29.aspx) <br/> |
|[Объект комментариев (Visio)](http://msdn.microsoft.com/library/7cd0ee53-6b8d-a03b-ecd6-f6f6dda0f2d4%28Office.15%29.aspx) <br/> |[Свойство Comments.Count (Visio)](http://msdn.microsoft.com/library/abac02d5-5047-2c9d-5c5c-e2738f99a4a6%28Office.15%29.aspx) <br/> [Свойство Comments.Document (Visio)](http://msdn.microsoft.com/library/507d4698-e282-f8a9-1299-c67945ee5fc4%28Office.15%29.aspx) <br/> [Свойство Comments.Item (Visio)](http://msdn.microsoft.com/library/fed2a079-de87-d5ce-1d74-0bfa5a328441%28Office.15%29.aspx) <br/> [Свойство Comments.ObjectType (Visio)](http://msdn.microsoft.com/library/06544d73-ce00-2c89-1ecb-20541b251d57%28Office.15%29.aspx) <br/> [Свойство Comments.Stat (Visio)](http://msdn.microsoft.com/library/1f5f29b2-236c-91b6-6d25-7bacc37ca96c%28Office.15%29.aspx) <br/> |[Метод Comments.Add (Visio)](http://msdn.microsoft.com/library/da02de49-8057-7e5c-6b59-0a013e56256d%28Office.15%29.aspx) <br/> [Метод Comments.DeleteAll (Visio)](http://msdn.microsoft.com/library/50777ed3-553c-90ae-2d30-9dde412fe6b9%28Office.15%29.aspx) <br/> |
|[Объект ReplaceShapesEvent (Visio)](http://msdn.microsoft.com/library/26c4e7cb-6618-6d2f-a4be-515584f8cd10%28Office.15%29.aspx) <br/> |[Свойство ReplaceShapesEvent.ObjectType (Visio)](http://msdn.microsoft.com/library/bcc442f0-aa4e-cd5a-d116-f3fb74459927%28Office.15%29.aspx) <br/> [Свойство ReplaceShapesEvent.ReplaceFlags (Visio)](http://msdn.microsoft.com/library/d0d00891-c794-bd0c-d37e-1ab98c92beab%28Office.15%29.aspx) <br/> [Свойство ReplaceShapesEvent.ReplacementMaster (Visio)](http://msdn.microsoft.com/library/326a1889-8952-b4ac-c5c0-ac4470257c06%28Office.15%29.aspx) <br/> [Свойство ReplaceShapesEvent.SelectionSource (Visio)](http://msdn.microsoft.com/library/f81c0b66-b63b-fc7c-1769-d56a17d5cf78%28Office.15%29.aspx) <br/> [Свойство ReplaceShapesEvent.Stat (Visio)](http://msdn.microsoft.com/library/96f3d382-5dda-7f93-088d-96edc831cd7c%28Office.15%29.aspx) <br/> |Нет  <br/> |
   
В следующей таблице перечислены новые перечисления и константы, введенные в Visio 2013.
  
 **В таблице 3. Перечисление дополнения Visio**
  
|**Перечисление**|**Описание**|
|:-----|:-----|
|[Перечисление VisQuickStyleColors (Visio)](http://msdn.microsoft.com/library/c19d91f3-a9a4-e31e-ed7a-eef15553fbf4%28Office.15%29.aspx) <br/> |Задает указанное имена для цвета, содержащиеся в теме.  <br/> |
|[Перечисление VisQuickStyleMatrixIndices (Visio)](http://msdn.microsoft.com/library/0fb0b448-85ba-4fc4-d933-21d574cefa2a%28Office.15%29.aspx) <br/> |Задает указанное имена тем и вариантов, входящие в состав Visio 2013.  <br/> |
|[Перечисление VisReplaceFlags (Visio)](http://msdn.microsoft.com/library/cf270178-f939-7eb4-b8e1-3b4153aff221%28Office.15%29.aspx) <br/> |Задает поведение для изменения фигуры операции.  <br/> |
|[Перечисление VisSVGExportFormat (Visio)](http://msdn.microsoft.com/library/d8ca8c3f-41d9-4e9d-8f6d-f5567361b14e%28Office.15%29.aspx) <br/> |Задает включение или исключение Visio разметки при экспорте схема SVG.  <br/> |
   
### <a name="deprecated-objects-and-members"></a>Устаревшие объекты и члены

В следующей таблице перечислены устаревшие объекты и члены, представленные в Visio 2013. Только устаревшие элементы перечисленные в столбце **устаревшие элементы** объекта. 
  
 **В таблице 4. Неподдерживаемые объектной модели Visio**
  
|**Объект или семейства сайтов**|**Устаревшие элементы**|
|:-----|:-----|
|Объект **Window**  <br/> |Свойство **PageTabWidth**  <br/> |
   
## <a name="see-also"></a>См. также
<a name="vis15_WhatsNew_Additional"> </a>

- [Visio для разработчиков (en)](http://msdn.microsoft.com/en-us/office/aa905478.aspx)
    
- [Новые возможности для разработчиков таблиц свойств фигур Visio](what-s-new-for-visio-shapesheet-developers.md)
    
- [Службы Visio в SharePoint 2013](http://msdn.microsoft.com/en-us/library/jj164027%28office.15%29.aspx)
    
- [Новые возможности Visio (Office.com)](http://office.com/redir/HA102749364.aspx)
    
- [Центр по разработке для Visio](http://msdn.microsoft.com/en-us/office/aa905478.aspx)
    

