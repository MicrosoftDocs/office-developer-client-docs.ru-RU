---
title: Элемент Window (Windows_Type ComplexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: da776276-e8c2-085b-9b23-e5b1f5ba64cd
description: Представляет открытое окно в экземпляре Microsoft Visio. Этот элемент содержит сведения, необходимые для точного повторного создания окна пользовательского интерфейса в рабочей области приложения при первоначальном Visio.
ms.openlocfilehash: 2700ee7a9a17460f6ac707f5b1a8f35d622e33e3
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538461"
---
# <a name="window-element-windows_type-complextype-visio-xml"></a>Элемент Window (Windows_Type ComplexType) (Visio XML)

Представляет открытое окно в экземпляре Microsoft Visio. Этот элемент содержит сведения, необходимые для точного повторного создания окна пользовательского интерфейса в рабочей области приложения при первоначальном Visio.
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[Window_Type](window_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Файл схемы** <br/> |VisioSchema15.xsd  <br/> |
|**Части документов** <br/> |windows.xml  <br/> |
   
## <a name="definition"></a>Определение

```XML
< xs:element name="Window" type="Window_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Элементы и атрибуты

Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений. 
  
### <a name="parent-elements"></a>Родительские элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[Windows](windows-elementvisio-xml.md) <br/> |[Windows_Type](windows_type-complextypevisio-xml.md) <br/> |Содержит **элементы Window** для документа.  <br/> |
   
### <a name="child-elements"></a>Дочерние элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[DynamicGridEnabled](dynamicgridenabled-element-window_type-complextypevisio-xml.md) <br/> |[DynamicGridEnabled_Type](dynamicgridenabled_type-complextypevisio-xml.md) <br/> |Указывает, включена ли функция динамической сетки для документа или окна.  <br/> |
|[GlueSettings](gluesettings-element-window_type-complextypevisio-xml.md) <br/> |[GlueSettings_Type](gluesettings_type-complextypevisio-xml.md) <br/> |Указывает объекты, которые формирует клей, когда клей включен в документе.  <br/> |
|[ShowConnectionPoints](showconnectionpoints-element-window_type-complextypevisio-xml.md) <br/> |[ShowConnectionPoints_Type](showconnectionpoints_type-complextypevisio-xml.md) <br/> |Указывает, показаны ли точки подключения в окне.  <br/> |
|[ShowGrid](showgrid-element-window_type-complextypevisio-xml.md) <br/> |[ShowGrid_Type](showgrid_type-complextypevisio-xml.md) <br/> |Указывает, отображается ли сетка в окне рисования.  <br/> |
|[ShowGuides](showguides-element-window_type-complextypevisio-xml.md) <br/> |[ShowGuides_Type](showguides_type-complextypevisio-xml.md) <br/> |Указывает, показаны ли руководства в окне рисования.  <br/> |
|[ShowPageBreaks](showpagebreaks-element-window_type-complextypevisio-xml.md) <br/> |[ShowPageBreaks_Type](showpagebreaks_type-complextypevisio-xml.md) <br/> |Указывает, показываются ли разрывы страниц в окне.  <br/> |
|[ShowRulers](showrulers-element-window_type-complextypevisio-xml.md) <br/> |[ShowRulers_Type](showrulers_type-complextypevisio-xml.md) <br/> |Указывает, показаны ли линейки в окне рисования.  <br/> |
|[SnapAngles](snapangles-element-window_type-complextypevisio-xml.md) <br/> |[SnapAngles_Type](snapangles_type-complextypevisio-xml.md) <br/> |Содержит коллекцию **элементов SnapAngle.**  <br/> |
|[SnapExtensions](snapextensions-element-window_type-complextypevisio-xml.md) <br/> |[SnapExtensions_Type](snapextensions_type-complextypevisio-xml.md) <br/> |Указывает, включен или отключен определенный параметр расширения оснастки для активного окна.  <br/> |
|[SnapSettings](snapsettings-element-window_type-complextypevisio-xml.md) <br/> |[SnapSettings_Type](snapsettings_type-complextypevisio-xml.md) <br/> |Указывает объекты, формуя привязку к при активной оснастке в окне.  <br/> |
|[StencilGroup](stencilgroup-element-window_type-complextypevisio-xml.md) <br/> |[StencilGroup_Type](stencilgroup_type-complextypevisio-xml.md) <br/> |Указывает группу слитого окна трафарета, членом которого является окно.  <br/> |
|[StencilGroupPos](stencilgrouppos-element-window_type-complextypevisio-xml.md) <br/> |[StencilGroupPos_Type](stencilgrouppos_type-complextypevisio-xml.md) <br/> |Содержит набор, который указывает относительное положение трафарета в группе в окне.  <br/> |
|[TabSplitterPos](tabsplitterpos-element-window_type-complextypevisio-xml.md) <br/> |[TabSplitterPos_Type](tabsplitterpos_type-complextypevisio-xml.md) <br/> |Указывает ширину управления вкладками страницы в окне рисования (в качестве доли от общей ширины окна рисования).  <br/> |
   
### <a name="attributes"></a>Атрибуты

|**Атрибут**|**Тип**|**Обязательный**|**Описание**|**Возможные значения**|
|:-----|:-----|:-----|:-----|:-----|
|Container  <br/> |xsd:unsignedInt  <br/> |необязательный  <br/> |ID контейнера: Page, Sheet или Master. Только релевантные и необходимые, **если задан ContainerType.**  <br/> |Значения типа xsd:unsignedInt.  <br/> |
|ContainerType  <br/> |xsd:token  <br/> |необязательный  <br/> |Может быть одним из следующих значений: Документ, Страница или Мастер. Релевантно только в том случае, если **WindowType** указывается как Drawing или Sheet.  <br/> |Значения типа xsd:token.  <br/> |
|Document  <br/> |xsd:string  <br/> |необязательный  <br/> |Путь файла документа, отображаемого в этом окне.  <br/> |Значения типа xsd:string.  <br/> |
|ID  <br/> |xsd:unsignedInt  <br/> |Обязательный  <br/> |Уникальный ID элемента в родительском элементе.  <br/> |Значения типа xsd:unsignedInt.  <br/> |
|Master  <br/> |xsd:unsignedInt  <br/> |необязательный  <br/> |Master ID, если в этом окне отображается мастер.  <br/> |Значения типа xsd:unsignedInt.  <br/> |
|Page  <br/> |xsd:unsignedInt  <br/> |необязательный  <br/> |ID страницы, если в этом окне отображается страница. Релевантно только в том случае, если **WindowType** указывается как Drawing и **ContainerType** , указывается как Page.  <br/> |Значения типа xsd:unsignedInt.  <br/> |
|ParentWindow  <br/> |xsd:unsignedInt  <br/> |необязательный  <br/> |ID окна, в котором содержится это окно трафарета. Актуально только при **указании WindowType** в качестве трафарета.  <br/> |Значения типа xsd:unsignedInt.  <br/> |
|ReadOnly  <br/> |xsd:boolean  <br/> |необязательный  <br/> |Флаг только для чтения, если этот трафарет не является трафаретом документа.  <br/> |Значения типа xsd:boolean.  <br/> |
|Таблица  <br/> |xsd:unsignedInt  <br/> |необязательный  <br/> |ID листа в контейнере. Релевантно только в том случае, если контейнер указан как Лист.  <br/> |Значения типа xsd:unsignedInt.  <br/> |
|ViewCenterX  <br/> |xsd:double  <br/> |необязательный  <br/> |**ViewCenterX** и **ViewCenterY** укажите точку центра на странице, которую предполагает новое представление (окно) при его первоначальном вскрытии.  <br/> |Значения типа xsd:double.  <br/> |
|ViewCenterY  <br/> |xsd:double  <br/> |необязательный  <br/> |**ViewCenterX** и **ViewCenterY** укажите точку центра на странице, которую предполагает новое представление (окно) при его первоначальном вскрытии.  <br/> |Значения типа xsd:double.  <br/> |
|ViewScale  <br/> |xsd:double  <br/> |необязательный  <br/> |Коэффициент увеличения по умолчанию, который используется при открывании нового представления (окна) страницы. Например, 1 = 100%; 1.5 = 150% и так далее.  <br/> |Значения типа xsd:double.  <br/> |
|WindowHeight  <br/> |xsd:unsignedInt  <br/> |необязательный  <br/> |Высота прямоугольника окна.  <br/> |Значения типа xsd:unsignedInt.  <br/> |
|WindowLeft  <br/> |xsd:short  <br/> |необязательный  <br/> |Левая координата прямоугольника окна.  <br/> |Значения xsd:short типа.  <br/> |
|WindowState  <br/> |xsd:unsignedInt  <br/> |необязательный  <br/> |Integer, указывающий битные флаги.  <br/> |Значения типа xsd:unsignedInt.  <br/> |
|WindowTop  <br/> |xsd:short  <br/> |необязательный  <br/> |Верхняя координата прямоугольника окна.  <br/> |Значения xsd:short типа.  <br/> |
|WindowType  <br/> |xsd:token  <br/> |Обязательный  <br/> |Это значение может быть одним из следующих: Drawing, Sheet, Stencil или Icon.  <br/> |Значения типа xsd:token.  <br/> |
|WindowWidth  <br/> |xsd:unsignedInt  <br/> |необязательный  <br/> |Ширина прямоугольника окна.  <br/> |Значения типа xsd:unsignedInt.  <br/> |
   

