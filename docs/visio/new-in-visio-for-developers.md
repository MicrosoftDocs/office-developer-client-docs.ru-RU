---
title: New in Visio for developers
manager: soliver
ms.date: 09/18/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 7e3fb858-0ab8-bd2e-217c-c85b10d79785
description: В этом документе представлено высокоуровневое представление расширений и дополнений для разработчиков в Visio 2013. Разработчикам, готовым к началу перехода на платформу Visio, предоставляется достаточно сведений для начала кодирования в Visio 2013.
ms.openlocfilehash: df4bc1fa493ee3976c99802400ee52691d05d20a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319819"
---
# <a name="new-in-visio-for-developers"></a>New in Visio for developers

В этом документе представлено высокоуровневое представление расширений и дополнений для разработчиков в Visio 2013. Разработчикам, готовым к началу перехода на платформу Visio, предоставляется достаточно сведений для начала кодирования в Visio 2013.
  
## <a name="introduction"></a>Введение
<a name="vis15_WhatsNew_Intro"> </a>

Visio 2013 предоставляет функциональную единую платформу для ваших документов. Новые объекты, коллекции, свойства, методы, перечисления и события, а также новые ячейки и функции таблицы свойств фигуры предоставляют дополнительные возможности для определения поведения элементов в решениях.
  
Новые функции, представляющие интерес для разработчиков в Visio 2013, представляют собой новый формат файлов; надежное обновление тем; Функция изменения фигуры (позволяет заменять фигуры на другие); новые эффекты фигур; улучшения в комментариях; Совместное редактирование в SharePoint Server 2013; Настраиваемая вырезка изображения; Относительная геометрия; Поддержка данных службы Business Connectivity Services (BCS); обновления служб Visio в Microsoft SharePoint Server 2013; и функция дублирования страниц. В этом разделе приведен краткий обзор каждой из этих функций и приводятся некоторые новые объекты Visio и элементы, связанные с этими функциями и предоставляемые в Visual Basic для приложений (VBA). Сведения об этих функциях и прилагаемых примерах кода можно найти в [центре разработчиков Visio](https://msdn.microsoft.com/office/aa905478.aspx).
  
> [!NOTE]
> Visio 2013 включает множество новых ячеек таблицы свойств фигуры, строк и функций для поддержки новых функций Visio. Для получения дополнительных сведений о новых возможностях таблицы свойств фигуры для Visio 2013, ознакомьтесь со статьей [новые возможности для разработчиков таблицы свойств фигуры Visio](what-s-new-for-visio-shapesheet-developers.md). 
  
## <a name="new-file-format"></a>Новый формат файла
<a name="vis15_WhatsNew_NewFF"> </a>

Visio 2013 включает новый формат файла, основанный на стандарте Open Packaging Conventions (OPC) (ISO 29500, часть 2), и XML-элементы из предыдущего формата файла Visio XML (VDX). Это формат ZIP-файл на основе XML, аналогичную форматы файлов, используемые в других приложениях .
  
Так как новый формат файлов поддерживается как в Visio 2013, так и в службах Visio в Microsoft SharePoint Server 2013, вы можете сохранить документ Visio непосредственно в библиотеке SharePoint Server, не публикуя его в качестве веб-документа Visio (. vdw). Тем не менее Службы Visio возможность чтения и отображение файлов веб-документа Visio.
  
Новый формат файлов содержит следующие типы файлов (по расширению).
  
- VSDX (документ Visio);
    
- VSDM (документ Visio с поддержкой макросов);
    
- VSSX (набор элементов Visio);
    
- VSSM (набор элементов Visio с поддержкой макросов);
    
- VSTX (шаблон Visio);
    
- VSTM (шаблон Visio с поддержкой макросов).
    
С помощью имеющейся поддержки чтения и записи в пакет формата файлов (например, [System. IO. Packaging](https://msdn.microsoft.com/library/System.IO.Packaging.aspx) ) и синтаксического анализа XML ( [System. XML. LINQ](https://msdn.microsoft.com/library/System.Xml.Linq.aspx) ) можно программно работать с новыми форматами файлов. 
  
В Visio 2013 сохраняется возможность чтения старых форматов файлов (VSD, VSS, ВСТ, vdx, VSX,. вткс,. VDW,. ВВИ). Visio 2013 не сохраняет файл в формате XML предыдущей версией Visio (VDX). Для чтения новых форматов файлов и их схем может потребоваться перепрограммировать решения и инструменты, которые используют предыдущие файлы формата XML-файлов Visio (VDX).
  
Службы Visio сохраняет возможность отображения в формат веб-документа Visio (.vdw) в браузере. Он теперь также выводит нового Visio документа (vsdx (en) и Visio макросами рисунка (.vsdm) форматы.
  
## <a name="themes"></a>Темы
<a name="vis15_WhatsNew_Themes"> </a>

В Visio 2013 темы изменены: расширен набор эффектов и стилей, включая интеграцию эффектов коллекций фигур. Теперь пользователи могут принять решение о наличии неизменного стиля, применив тему, персонализировать схему с помощью вариантов тем и выделить отдельные фигуры с помощью экспрессных стилей. Разработчики таблицы свойств фигуры могут использовать эти функции с новыми функциями и ячейками в таблице свойств фигуры.
  
Вы также можете управлять темами на уровне [страницы](https://msdn.microsoft.com/library/7a7f37ab-b448-eb70-b4f1-c185dfbd511e%28Office.15%29.aspx), [фигуры](https://msdn.microsoft.com/library/da7a8872-4ebb-a607-e0ed-eebf68ff5630%28Office.15%29.aspx)и объекта [Selection](https://msdn.microsoft.com/library/e5734140-6dbe-7de8-9695-1a22fb4ac628%28Office.15%29.aspx) . Новые API для работы с темами включают метод [Page. сетсеме](https://msdn.microsoft.com/library/5a186f58-9a7a-bd8a-826b-85da75a4d59f%28Office.15%29.aspx) , [Page. Сетсемевариант](https://msdn.microsoft.com/library/8393a95f-83ca-0efa-d987-ae498bfe5e9d%28Office.15%29.aspx) , метод [Shape. Сеткуиккстиле](https://msdn.microsoft.com/library/aebe80cb-fae9-0be7-e903-882f6eb58b63%28Office.15%29.aspx) и метод [Selection. сеткуиккстиле](https://msdn.microsoft.com/library/39b810b5-0738-daed-0103-8a2df07559c6%28Office.15%29.aspx) . 
  
Подробный список новых API-интерфейсов в Visio 2013 вы найдете в разделе [изменения объектной модели Visio](#vis15_WhatsNew_NewOM) этой статьи. Дополнительные сведения о новых ячейках таблицы свойств фигуры в Visio 2013 вы найдете в статье [новые возможности для разработчиков таблицы свойств фигуры Visio](what-s-new-for-visio-shapesheet-developers.md).
  
## <a name="change-shape"></a>Изменение фигуры
<a name="vis15_WhatsNew_ChangeShapes"> </a>

В Visio 2013 есть API замены фигур, который позволяет переключать одну или несколько фигур для другой фигуры, содержащейся в трафарете, сохраняя некоторые локальные значения исходной фигуры, такие как фигура текста фигуры, данные фигуры или Форматирование фигуры. Разработчики фигур могут обновить параметры таблицы свойств фигуры для своих собственных фигур, чтобы указать поведение фигуры изменить для своих фигур. Среди новых API представлены методы [Shape. реплацешапес](https://msdn.microsoft.com/library/b330a63d-4e3f-0c4d-c38c-6ee806670225%28Office.15%29.aspx) и [Selection. реплацешапес](https://msdn.microsoft.com/library/dc278901-77ce-e1fe-c44f-f464bbb1c360%28Office.15%29.aspx) , а также событие [реплацешапе](https://msdn.microsoft.com/library/26c4e7cb-6618-6d2f-a4be-515584f8cd10%28Office.15%29.aspx) . 
  
Подробный список новых API-интерфейсов в Visio 2013 вы найдете в разделе [изменения объектной модели Visio](#vis15_WhatsNew_NewOM) этой статьи. Дополнительные сведения о новых ячейках таблицы свойств фигуры в Visio 2013 вы найдете в статье [новые возможности для разработчиков таблицы свойств фигуры Visio](what-s-new-for-visio-shapesheet-developers.md).
  
## <a name="shape-effects"></a>Эффекты фигур
<a name="vis15_WhatsNew_ShapeEffects"> </a>

Новые эффекты фигур, такие как багетная рамка, трехмерное вращение, свечение, отражение и эскизы, были добавлены в Visio 2013. Таблица свойств фигуры включает новые ячейки для работы с этими влияниями.
  
Дополнительные сведения о новых ячейках таблицы свойств фигуры в Visio 2013 вы найдете в статье [новые возможности для разработчиков таблицы свойств фигуры Visio](what-s-new-for-visio-shapesheet-developers.md).
  
## <a name="commenting"></a>Комментарии
<a name="vis15_WhatsNew_Commenting"> </a>

Visio 2013 включает в себя новые комментирования framework. Комментарии, теперь могут быть связаны с конкретной формы или страницы. Visio 2013 включает два новых объекта, [Комментарии](https://msdn.microsoft.com/library/f028cc03-0ef1-8017-a936-d30d45211864%28Office.15%29.aspx) и [](https://msdn.microsoft.com/library/7cd0ee53-6b8d-a03b-ecd6-f6f6dda0f2d4%28Office.15%29.aspx)комментарии. Новые API для доступа к комментариям программными средствами включают свойства [Document. Comments](https://msdn.microsoft.com/library/15a322ad-70eb-1487-701d-76e2fde73309%28Office.15%29.aspx), [Page. Comments](https://msdn.microsoft.com/library/9618c86c-96c0-be95-ee20-5d1b99f4d5e8%28Office.15%29.aspx), [Shape. Comments](https://msdn.microsoft.com/library/498eca91-beb9-b764-0262-a935e5205710%28Office.15%29.aspx)и [Page. шапекомментс](https://msdn.microsoft.com/library/b7d86594-ba1f-627b-222f-905da1b1201e%28Office.15%29.aspx) . 
  
Службы Visio включают API JavaScript для чтения комментариев со страницы или фигуры в схеме.
  
Подробный список новых API-интерфейсов в Visio 2013 вы найдете в разделе [изменения объектной модели Visio](#vis15_WhatsNew_NewOM) этой статьи. 
  
> [!NOTE]
> Комментарии больше недоступны в таблице свойств фигуры. 
  
## <a name="coauthoring"></a>Совместное редактирование
<a name="vis15_WhatsNew_Coauthoring"> </a>

Visio 2013 содержит возможность совместного редактирования схем, хранящихся в SharePoint или Microsoft OneDrive. Разработчики имеют доступ к событию [Document. афтердокументмерже](https://msdn.microsoft.com/library/50658da5-592a-4d16-908f-c6abe3050f09%28Office.15%29.aspx) , которое предоставляет сведения об изменениях в схеме из-за совместного редактирования. Разработчики решений также могут отключить совместное редактирование в соответствии с собственными потребностями с помощью ячейки [NoCoauth](nocoauth-cell-document-properties-section.md) в таблице свойств фигуры. 
  
Подробный список новых API-интерфейсов в Visio 2013 вы найдете в разделе [изменения объектной модели Visio](#vis15_WhatsNew_NewOM) этой статьи. 
  
## <a name="customizable-image-clipping"></a>Настраиваемое кадрирование изображений
<a name="vis15_WhatsNew_ClipImages"> </a>

Visio 2013 поддерживает задание настраиваемого контура кадрирования изображения, который позволяет обрезать изображения до любой формы. Это расширяет емкость Visio 2010, которая поддерживает обрезание изображений в прямоугольном виде. Эта функциональная возможность доступна в таблице свойств фигуры с помощью ячейки [ClippingPath](clippingpath-cell-foreign-image-info-section.md) в разделе **сведения о внешнем изображении** . 
  
Дополнительные сведения о новых ячейках таблицы свойств фигуры в Visio 2013 вы найдете в статье [новые возможности для разработчиков таблицы свойств фигуры Visio](what-s-new-for-visio-shapesheet-developers.md).
  
## <a name="relative-geometries"></a>Относительная геометрия
<a name="vis15_WhatsNew_RelativeGeometry"> </a>

В предыдущих версиях Visio геометрические фигуры были определены формулами, которые зависят от высоты или ширины фигуры. Например, в Visio 2010 вершины многих встроенных фигур Visio были определены путем умножения высоты или ширины фигуры на константу. Эти фигуры содержат **** геометрические разделы, включающие строки [MoveTo](moveto-row-geometry-section.md) или [lineTo](lineto-row-geometry-section.md) (например,) `Width*1` с `Height*0`помощью формул, таких как и.
  
Visio 2013 теперь поддерживает относительную геометрию в таблице свойств фигуры. Теперь разработчики фигур могут использовать относительные геометрические фигуры, чтобы указать геометрические фигуры как простые значения или формулы, которые автоматически умножаются на высоту или ширину. В качестве вершин фигуры теперь можно выражать константы, что позволяет удалять вершины в виде множителей ширины или высоты фигуры. Это облегчает разработчикам создание фигур, а также повышает производительность и уменьшает размер файлов. К новым строкам относятся строки [строка relmoveto](relmoveto-row-geometry-section.md) и [строка rellineto](rellineto-row-geometry-section.md) , в которых значения ячеек **X** и **Y** автоматически умножаются на ширину или высоту фигуры (соответственно). 
  
Дополнительные сведения о новых строках таблицы свойств фигуры в Visio 2013 вы найдете в статье [новые возможности для разработчиков таблицы свойств фигуры Visio](what-s-new-for-visio-shapesheet-developers.md).
  
## <a name="support-for-business-connectivity-services-bcs-data"></a>Поддержка данных Business Connectivity Services (BCS)
<a name="vis15_WhatsNew_BCS"> </a>

Теперь схемы Visio 2013 могут быть подключены к внешним спискам на серверах SharePoint Server 2013. Внешний список — это источник контента, который является внешним по отношению к SharePoint (например, таблица SQL Server), подключенный к списку SharePoint с помощью Microsoft Business Connectivity Services (BCS). Службы Visio поддерживает возможность обновления схемы Visio как обновления данных.
  
Для получения дополнительных сведений о новых возможностях служб Visio ознакомьтесь со статьей [службы Visio в SharePoint 2013](https://msdn.microsoft.com/library/jj164027%28office.15%29.aspx). Для получения дополнительных сведений о Business Connectivity Services (BCS) ознакомьтесь со статьей [Business Connectivity Services в SharePoint 2013](https://msdn.microsoft.com/library/jj163782%28office.15%29.aspx).
  
## <a name="improvements-in-visio-services"></a>Улучшения в службах Visio
<a name="vis15_WhatsNew_VisioServices"> </a>

Службы Visio в Microsoft SharePoint Server 2013 включают множество улучшений. Как упоминалось ранее, службы Visio поддерживают новый формат файлов Visio (как для vsdx, так и для vsdm). Службы Visio расширяют возможности обновления данных и пересчета, включая возможность пересчета формул во всей диаграмме. 
  
Для получения дополнительных сведений о новых возможностях служб Visio ознакомьтесь со статьей [службы Visio в SharePoint 2013](https://msdn.microsoft.com/library/jj164027%28office.15%29.aspx).
  
## <a name="duplicate-page"></a>Повторяющаяся страница
<a name="vis15_WhatsNew_DuplicatePage"> </a>

Теперь вы можете скопировать страницу и все ее фигуры в одном документе в Visio 2013. Соответственно, объект **Page** содержит новый метод, повторяется [](https://msdn.microsoft.com/library/394be23b-997d-0da1-b3bd-8278564fb4e0%28Office.15%29.aspx), который дублирует страницу и возвращает новый объект **Page** . 
  
## <a name="visio-object-model-changes"></a>Изменения объектной модели Visio
<a name="vis15_WhatsNew_NewOM"> </a>

Новые объекты, свойства, методы и события, добавленные в объектную модель Visio, обеспечивают поддержку программирования для новых функций Visio 2013. Кроме того, улучшения в объектной модели устраняют частые запросы разработчиков на изменения платформы Visio.
  
### <a name="new-members"></a>Новые элементы

Следующие элементы были добавлены к существующим объектам в объектной модели Visio.
  
 **Таблица 1. Расширения объектной модели Visio**
  
|**Объект или коллекция**|**Новые члены**|
|:-----|:-----|
|[Объект Application (Visio)](https://msdn.microsoft.com/library/5b3c8939-793f-116f-11b8-1d4170d95a63%28Office.15%29.aspx) <br/> |[Событие Application. Афтерреплацешапес (Visio)](https://msdn.microsoft.com/library/b02de031-086a-41cc-d832-5434b8096444%28Office.15%29.aspx) <br/> |
||[Событие Application. Бефоререплацешапес (Visio)](https://msdn.microsoft.com/library/fbf44569-0539-9292-ce20-1f9e34238b33%28Office.15%29.aspx) <br/> |
||[Событие Application. Куериканцелреплацешапес (Visio)](https://msdn.microsoft.com/library/50c0f2a6-f534-f3af-7e83-c865abda8bf9%28Office.15%29.aspx) <br/> |
||[Событие Application. Реплацешапесканцелед (Visio)](https://msdn.microsoft.com/library/e8eecd64-e4bd-d2c4-b942-c5ff607a4121%28Office.15%29.aspx) <br/> |
|[Объект ApplicationSettings (Visio)](https://msdn.microsoft.com/library/f2e24211-ecc6-e0f5-4c00-fc50f98a3505%28Office.15%29.aspx) <br/> |[Свойство ApplicationSettings. Ентеркоммитстекст (Visio)](https://msdn.microsoft.com/library/ba9ce9fa-d224-cdc3-668d-46c1849911c7%28Office.15%29.aspx) <br/> |
||[Свойство ApplicationSettings. Свжекспортформат (Visio)](https://msdn.microsoft.com/library/9e7ca1cb-5ace-b75b-0e59-61566b9a0169%28Office.15%29.aspx) <br/> |
|[Объект Document (Visio)](https://msdn.microsoft.com/library/21640062-13a2-a2b2-7c61-7e707671207c%28Office.15%29.aspx) <br/> |[Событие Document. Афтердокументмерже (Visio)](https://msdn.microsoft.com/library/50658da5-592a-4d16-908f-c6abe3050f09%28Office.15%29.aspx) <br/> |
||[Свойство Document. Comments (Visio)](https://msdn.microsoft.com/library/15a322ad-70eb-1487-701d-76e2fde73309%28Office.15%29.aspx) <br/> |
||[Свойство Document. Компатибилитимоде (Visio)](https://msdn.microsoft.com/library/98fc00d3-5d2b-218e-9828-b5581ee7313d%28Office.15%29.aspx) <br/> |
|[Объект Documents (Visio)](https://msdn.microsoft.com/library/e9291149-964e-c6fb-4c62-bf2f35a6a0a7%28Office.15%29.aspx) <br/> |[Событие Documents. Афтердокументмерже (Visio)](https://msdn.microsoft.com/library/cac0544d-77b9-b722-cfdb-e42475ce2558%28Office.15%29.aspx) <br/> |
||[Событие Documents. Афтерреплацешапес (Visio)](https://msdn.microsoft.com/library/e01c069e-440b-7b8b-8d7d-cdb664f6e2d6%28Office.15%29.aspx) <br/> |
||[Событие Documents. Бефоререплацешапес (Visio)](https://msdn.microsoft.com/library/55a66c47-a2ca-5c8a-2693-aaa1b079c704%28Office.15%29.aspx) <br/> |
||[Событие Documents. Куериканцелреплацешапес (Visio)](https://msdn.microsoft.com/library/d613730e-04c8-d17f-0ad1-19e976aa107d%28Office.15%29.aspx) <br/> |
||[Событие Documents. Реплацешапесканцелед (Visio)](https://msdn.microsoft.com/library/94a20fe7-da09-4e3c-d048-05ba0b8f1070%28Office.15%29.aspx) <br/> |
|[Объект InvisibleApp (Visio)](https://msdn.microsoft.com/library/70a30571-2017-af8b-eaa1-bf93c758a46a%28Office.15%29.aspx) <br/> |[Событие InvisibleApp. Афтерреплацешапес (Visio)](https://msdn.microsoft.com/library/5d7b8ec2-ef65-1a49-fb50-3fae95d56761%28Office.15%29.aspx) <br/> |
||[Событие InvisibleApp. Бефоререплацешапес (Visio)](https://msdn.microsoft.com/library/bd0e37ca-887a-4d53-3b0c-3339492df3dd%28Office.15%29.aspx) <br/> |
||[Событие InvisibleApp. Куериканцелреплацешапес (Visio)](https://msdn.microsoft.com/library/5e5d9b76-dfd4-1d02-d205-9e64350449d5%28Office.15%29.aspx) <br/> |
||[Событие InvisibleApp. Реплацешапесканцелед (Visio)](https://msdn.microsoft.com/library/17e43497-c7a8-8546-595c-4630afb301a3%28Office.15%29.aspx) <br/> |
|[Объект Page (Visio)](https://msdn.microsoft.com/library/7a7f37ab-b448-eb70-b4f1-c185dfbd511e%28Office.15%29.aspx) <br/> |[Событие Page. Афтерреплацешапес (Visio)](https://msdn.microsoft.com/library/e4005987-acb1-78d7-91fb-c3c2d5b036e3%28Office.15%29.aspx) <br/> |
||[Событие Page. Бефоререплацешапес (Visio)](https://msdn.microsoft.com/library/57ea9836-74dd-77c2-6541-f8f61b89c0b6%28Office.15%29.aspx) <br/> |
||[Свойство Page. Comments (Visio)](https://msdn.microsoft.com/library/9618c86c-96c0-be95-ee20-5d1b99f4d5e8%28Office.15%29.aspx) <br/> |
||[Метод Page. дублирует (Visio)](https://msdn.microsoft.com/library/394be23b-997d-0da1-b3bd-8278564fb4e0%28Office.15%29.aspx) <br/> |
||[Метод Page. метод Page (Visio)](https://msdn.microsoft.com/library/31c84e69-0bc8-2d1a-84d8-7397110d74ae%28Office.15%29.aspx) <br/> |
||[Метод Page. Жетсемевариант (Visio)](https://msdn.microsoft.com/library/40c2be31-fdb0-68ee-a129-2788b1b17c82%28Office.15%29.aspx) <br/> |
||[Событие Page. Куериканцелреплацешапес (Visio)](https://msdn.microsoft.com/library/17ead23f-825a-c608-3315-e2eed6784cd5%28Office.15%29.aspx) <br/> |
||[Событие Page. Реплацешапесканцелед (Visio)](https://msdn.microsoft.com/library/867b1fc1-96bd-cbeb-fd61-b02a96e039ca%28Office.15%29.aspx) <br/> |
||[Метод Page. Сетсеме (Visio)](https://msdn.microsoft.com/library/5a186f58-9a7a-bd8a-826b-85da75a4d59f%28Office.15%29.aspx) <br/> |
||[Метод Page. Сетсемевариант (Visio)](https://msdn.microsoft.com/library/8393a95f-83ca-0efa-d987-ae498bfe5e9d%28Office.15%29.aspx) <br/> |
||[Свойство Page. Шапекомментс (Visio)](https://msdn.microsoft.com/library/b7d86594-ba1f-627b-222f-905da1b1201e%28Office.15%29.aspx) <br/> |
|[Объект Pages (Visio)](https://msdn.microsoft.com/library/45eec568-b5cc-5e80-ff5c-4dfa567efb5d%28Office.15%29.aspx) <br/> |[Событие Pages. Афтерреплацешапес (Visio)](https://msdn.microsoft.com/library/05c33bdd-e697-d36e-46a8-45705e9ad2c2%28Office.15%29.aspx) <br/> |
||[Событие Pages. Бефоререплацешапес (Visio)](https://msdn.microsoft.com/library/3f6dbc31-0583-dd67-0432-335d6df7a50c%28Office.15%29.aspx) <br/> |
||[Событие Pages. Куериканцелреплацешапес (Visio)](https://msdn.microsoft.com/library/d11ff976-0016-da6b-92fb-379baa7e8f94%28Office.15%29.aspx) <br/> |
||[Событие Pages. Реплацешапесканцелед (Visio)](https://msdn.microsoft.com/library/f0ce8c66-7a15-5f91-8c89-e177bc6671d2%28Office.15%29.aspx) <br/> |
|[Объект Selection (Visio)](https://msdn.microsoft.com/library/e5734140-6dbe-7de8-9695-1a22fb4ac628%28Office.15%29.aspx) <br/> |[Метод Selection. Реплацешапе (Visio)](https://msdn.microsoft.com/library/dc278901-77ce-e1fe-c44f-f464bbb1c360%28Office.15%29.aspx) <br/> |
||[Метод Selection. Сеткуиккстиле (Visio)](https://msdn.microsoft.com/library/39b810b5-0738-daed-0103-8a2df07559c6%28Office.15%29.aspx) <br/> |
|[Объект Shape (Visio)](https://msdn.microsoft.com/library/da7a8872-4ebb-a607-e0ed-eebf68ff5630%28Office.15%29.aspx) <br/> |[Метод Shape. Чанжепиктуре (Visio)](https://msdn.microsoft.com/library/9193d802-cebd-2bfd-5f8e-400fac36c1a5%28Office.15%29.aspx) <br/> |
||[Свойство Shape. Comments (Visio)](https://msdn.microsoft.com/library/498eca91-beb9-b764-0262-a935e5205710%28Office.15%29.aspx) <br/> |
||[Метод Shape. Реплацешапе (Visio)](https://msdn.microsoft.com/library/b330a63d-4e3f-0c4d-c38c-6ee806670225%28Office.15%29.aspx) <br/> |
||[Метод Shape. Сеткуиккстиле (Visio)](https://msdn.microsoft.com/library/aebe80cb-fae9-0be7-e903-882f6eb58b63%28Office.15%29.aspx) <br/> |
   
### <a name="new-objects-and-enumerations"></a>Новые объекты и перечисления

В объектной модели Visio были добавлены следующие объекты.
  
 **Таблица 2. Добавление объектов в объектной модели Visio**
  
|**Object**|**Свойства**|**Методы**|
|:-----|:-----|:-----|
|[Объект CoauthMergeEvent (Visio)](https://msdn.microsoft.com/library/eb9425cb-0108-4909-e334-9cd51e5b9303%28Office.15%29.aspx) <br/> |[Свойство CoauthMergeEvent. Баседокумент (Visio)](https://msdn.microsoft.com/library/7ec09a85-6f51-685b-0c87-4b9eb3266773%28Office.15%29.aspx) <br/> [Свойство CoauthMergeEvent. Довнлоаддокумент (Visio)](https://msdn.microsoft.com/library/19239540-cd5a-13ea-3b26-282ac3676abd%28Office.15%29.aspx) <br/> [Свойство CoauthMergeEvent. ObjectType (Visio)](https://msdn.microsoft.com/library/01baa0c2-75b7-2713-9732-1e7a8a7b33aa%28Office.15%29.aspx) <br/> [Свойство CoauthMergeEvent. stat (Visio)](https://msdn.microsoft.com/library/d8a96b8e-36b5-c61f-8cea-76266f7eed39%28Office.15%29.aspx) <br/> [Свойство CoauthMergeEvent. Воркингдокумент (Visio)](https://msdn.microsoft.com/library/0f3c4358-0d63-df7f-12fe-7f378bacca86%28Office.15%29.aspx) <br/> |Нет  <br/> |
|[Объект Comment (Visio)](https://msdn.microsoft.com/library/f028cc03-0ef1-8017-a936-d30d45211864%28Office.15%29.aspx) <br/> |[Свойство Comment. АссоЦиатедобжект (Visio)](https://msdn.microsoft.com/library/e28eed2e-260e-59c9-9b24-631817fe1ae1%28Office.15%29.aspx) <br/> [Свойство Comment. Аусоринитиалс (Visio)](https://msdn.microsoft.com/library/abc07100-8c5c-9982-674d-40b58c096816%28Office.15%29.aspx) <br/> [Свойство Comment. Аусорнаме (Visio)](https://msdn.microsoft.com/library/e1da4db8-7a16-16bf-2a5f-be1ac5372d34%28Office.15%29.aspx) <br/> [Свойство Comment. Аусорсипаддресс (Visio)](https://msdn.microsoft.com/library/f8d185a9-91b6-471a-3c0e-ffa8a06b36b3%28Office.15%29.aspx) <br/> [Свойство Comment. Аусорсмтпаддресс (Visio)](https://msdn.microsoft.com/library/22e04ccc-c524-ca08-d5e2-db68fdb3afb6%28Office.15%29.aspx) <br/> [Свойство Comment. свернуто (Visio)](https://msdn.microsoft.com/library/9552e379-e351-78d7-e0ed-4f524c3273a1%28Office.15%29.aspx) <br/> [Свойство Comment. Креатедате (Visio)](https://msdn.microsoft.com/library/b643e13e-da12-a992-3a59-99b37f003fb9%28Office.15%29.aspx) <br/> [Свойство Comment. Document (Visio)](https://msdn.microsoft.com/library/d57b1377-b895-1fe1-2f98-ef000fdd9c39%28Office.15%29.aspx) <br/> [Свойство Comment. Едитдате (Visio)](https://msdn.microsoft.com/library/4ad13f54-215e-3680-5de6-13715e309fbf%28Office.15%29.aspx) <br/> [Свойство Comment. ObjectType (Visio)](https://msdn.microsoft.com/library/bf0d786d-e1b6-65f1-3112-5dfd4ff324e9%28Office.15%29.aspx) <br/> [Свойство Comment. stat (Visio)](https://msdn.microsoft.com/library/f457598c-af42-cb83-ecd2-4fd42898ea16%28Office.15%29.aspx) <br/> [Свойство Comment. Text (Visio)](https://msdn.microsoft.com/library/3ec63034-de5f-d9f2-16a5-e06a56883867%28Office.15%29.aspx) <br/> |[Метод Comment. Delete (Visio)](https://msdn.microsoft.com/library/7762f264-f680-5758-7c35-dfe9067b61ca%28Office.15%29.aspx) <br/> |
|[Объект Comments (Visio)](https://msdn.microsoft.com/library/7cd0ee53-6b8d-a03b-ecd6-f6f6dda0f2d4%28Office.15%29.aspx) <br/> |[Свойство Comments. Count (Visio)](https://msdn.microsoft.com/library/abac02d5-5047-2c9d-5c5c-e2738f99a4a6%28Office.15%29.aspx) <br/> [Свойство Comments. Document (Visio)](https://msdn.microsoft.com/library/507d4698-e282-f8a9-1299-c67945ee5fc4%28Office.15%29.aspx) <br/> [Свойство Comments. Item (Visio)](https://msdn.microsoft.com/library/fed2a079-de87-d5ce-1d74-0bfa5a328441%28Office.15%29.aspx) <br/> [Свойство Comments. ObjectType (Visio)](https://msdn.microsoft.com/library/06544d73-ce00-2c89-1ecb-20541b251d57%28Office.15%29.aspx) <br/> [Свойство Comments. stat (Visio)](https://msdn.microsoft.com/library/1f5f29b2-236c-91b6-6d25-7bacc37ca96c%28Office.15%29.aspx) <br/> |[Метод Comments. Add (Visio)](https://msdn.microsoft.com/library/da02de49-8057-7e5c-6b59-0a013e56256d%28Office.15%29.aspx) <br/> [Метод Comments. DeleteAll (Visio)](https://msdn.microsoft.com/library/50777ed3-553c-90ae-2d30-9dde412fe6b9%28Office.15%29.aspx) <br/> |
|[Объект ReplaceShapesEvent (Visio)](https://msdn.microsoft.com/library/26c4e7cb-6618-6d2f-a4be-515584f8cd10%28Office.15%29.aspx) <br/> |[Свойство ReplaceShapesEvent. ObjectType (Visio)](https://msdn.microsoft.com/library/bcc442f0-aa4e-cd5a-d116-f3fb74459927%28Office.15%29.aspx) <br/> [Свойство ReplaceShapesEvent. Реплацефлагс (Visio)](https://msdn.microsoft.com/library/d0d00891-c794-bd0c-d37e-1ab98c92beab%28Office.15%29.aspx) <br/> [Свойство ReplaceShapesEvent. Реплацементмастер (Visio)](https://msdn.microsoft.com/library/326a1889-8952-b4ac-c5c0-ac4470257c06%28Office.15%29.aspx) <br/> [Свойство ReplaceShapesEvent. Селектионсаурце (Visio)](https://msdn.microsoft.com/library/f81c0b66-b63b-fc7c-1769-d56a17d5cf78%28Office.15%29.aspx) <br/> [Свойство ReplaceShapesEvent. stat (Visio)](https://msdn.microsoft.com/library/96f3d382-5dda-7f93-088d-96edc831cd7c%28Office.15%29.aspx) <br/> |Нет  <br/> |
   
В следующей таблице перечислены новые перечисления и константы, представленные в Visio 2013.
  
 **Таблица 3. Дополнения перечисления Visio**
  
|**Перечисление**|**Описание**|
|:-----|:-----|
|[ПереЧисление Вискуиккстилеколорс (Visio)](https://msdn.microsoft.com/library/c19d91f3-a9a4-e31e-ed7a-eef15553fbf4%28Office.15%29.aspx) <br/> |Задает назначенные имена для цветов, содержащихся в теме.  <br/> |
|[ПереЧисление Вискуиккстилематриксиндицес (Visio)](https://msdn.microsoft.com/library/0fb0b448-85ba-4fc4-d933-21d574cefa2a%28Office.15%29.aspx) <br/> |Задает назначенные имена тем и вариантов, предоставленных в Visio 2013.  <br/> |
|[ПереЧисление Висреплацефлагс (Visio)](https://msdn.microsoft.com/library/cf270178-f939-7eb4-b8e1-3b4153aff221%28Office.15%29.aspx) <br/> |Задает поведение для операции изменения фигуры.  <br/> |
|[ПереЧисление Виссвжекспортформат (Visio)](https://msdn.microsoft.com/library/d8ca8c3f-41d9-4e9d-8f6d-f5567361b14e%28Office.15%29.aspx) <br/> |Указывает включение или исключение разметки Visio при экспорте схемы в формат SVG.  <br/> |
   
### <a name="deprecated-objects-and-members"></a>Устаревшие объекты и элементы

В следующей таблице перечислены устаревшие объекты и элементы, представленные в Visio 2013. В столбце " **устаревшие элементы** " перечислены только устаревшие элементы объекта. 
  
 **Таблица 4. Устаревшие объекты в объектной модели Visio**
  
|**Объект или коллекция**|**Устаревшие элементы**|
|:-----|:-----|
|Объект **Window**  <br/> |Свойство **пажетабвидс**  <br/> |
   
## <a name="see-also"></a>См. также
<a name="vis15_WhatsNew_Additional"> </a>

- [Visio для разработчиков](https://msdn.microsoft.com/office/aa905478.aspx)
    
- [Новые возможности для разработчиков таблиц свойств фигур Visio](what-s-new-for-visio-shapesheet-developers.md)
    
- [Службы Visio в SharePoint 2013](https://msdn.microsoft.com/library/jj164027%28office.15%29.aspx)
    
- [Новые возможности в Visio (Office.com)](https://office.com/redir/HA102749364.aspx)
    
- [Центр по разработке для Visio](https://msdn.microsoft.com/office/aa905478.aspx)
    

