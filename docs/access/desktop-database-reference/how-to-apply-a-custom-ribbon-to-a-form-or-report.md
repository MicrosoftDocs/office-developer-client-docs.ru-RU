---
title: Применение настраиваемой ленты в форму или отчет
TOCTitle: Apply a custom ribbon to a form or report
ms:assetid: 7dcdfa42-3eaa-43f9-b99d-56b2cac97f84
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196428(v=office.15)
ms:contentKeyID: 48545865
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f4fb0155b1a1ed36b6fe924f72a4da385197cc21
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25482357"
---
# <a name="apply-a-custom-ribbon-to-a-form-or-report"></a>Применение настраиваемой ленты в форму или отчет


**Применимо к**: Access 2013 | Office 2013

Ленты использует текстовую декларативную разметку XML, упрощающую создание и настройку ленты. С помощью нескольких строк XML можно создать только что правом интерфейс для пользователя. Access обеспечивает гибкость при настройке пользовательского интерфейса ленты. Например разметку для настройки может быть хранятся в таблице, внедренные в процедуре VBA, хранящиеся в другую базу данных Access или по ссылке из листа Excel. В этом разделе описывается применение настроенной ленты при загрузке формы или отчета.

## <a name="making-the-ribbon-customization-xml-available"></a>Предоставление XML настройки ленты

**Хранение расширяемость ленты XML в таблице**

— Это один метод, который можно использовать для настройки ленты доступны для их хранения в таблице. При сохранении настроек в таблице с именем **USysRibbons**настроек может быть реализовано без с помощью макросов или кода VBA.

**USysRibbons** — это таблица системы, созданные пользователем. В таблице должны быть созданы с помощью имена определенных столбцов в порядке для настройки ленты для реализации. В следующей таблице перечислены параметры для использования при создании в таблице **USysRibbons** .

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Имя столбца</p></th>
<th><p>Тип данных</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>RibbonName</strong></p></td>
<td><p>Текст</p></td>
<td><p>Содержит имя настраиваемой ленты, который будет связан с этой настройкой</p></td>
</tr>
<tr class="even">
<td><p><strong>RibbonXML</strong></p></td>
<td><p>Заметка</p></td>
<td><p>Содержит расширения XML-кодом ленты (RibbonX), который определяет настройки ленты</p></td>
</tr>
</tbody>
</table>


**Загрузка расширяемость XML ленты программными средствами**

Можно использовать метод **[LoadCustomUI](https://msdn.microsoft.com/library/ff194416\(v=office.15\))** для загрузки настроек ленты программными средствами. Как правило чтобы создать и становится доступной для приложения ленты, сначала создайте модуль в базе данных с помощью процедуры, вызывающий метод **LoadCustomUI** , передавая имя ленты и разметки XML для настройки.

XML-разметка могут поступать из объекта **набора записей** , созданных из таблицы, из источника, внешними по отношению к базы данных, например XML-файл, который проанализировать в строку или из XML-разметка внедрена непосредственно в процедуру. Можно выполнять различные ленты с помощью нескольких звонков на метод **LoadCustomUI** , передав в различных XML-разметка, поскольку имя каждой ленты и вкладки, которые составляют ленты для атрибута **id** — уникальный.

После завершения процедуры нажмите Создать макрос AutoExec, который вызывает процедуру с использованием действием RunCode. Таким образом, при запуске приложения метод **LoadCustomUI** выполняется автоматически и все настраиваемые ленты доступны для приложения.

## <a name="assigning-custom-ribbons-to-forms-or-reports"></a>Назначение настраиваемой ленты для форм и отчетов

1.  Выполните действия, описанные выше, чтобы сделать доступным для приложения настраиваемой ленты.

2.  Откройте форму или отчет в режиме конструктора.

3.  На вкладке "Конструктор" нажмите кнопку **Свойств**.

4.  На вкладке **все** окна Свойства выберите в списке **Имя ленты** и выберите ленты.

5.  Сохраните, закройте и снова откройте форму или отчет. Отображается пользовательский Интерфейс, выбранный ленты.


> [!NOTE]
> Вкладки на ленте пользовательского интерфейса-дополнительная. То есть до специально скрытия вкладки или *с самого начала* атрибуту присваивается **значение True**, вкладки отображаются в форме или пользовательского интерфейса ленты отчета, в дополнение к существующих вкладок.

> [!NOTE]
> Дополнительные сведения о пользовательский Интерфейс ленты в других приложениях Office можно [Обзор ленты Office Fluent](https://docs.microsoft.com/office/vba/Library-Reference/Concepts/overview-of-the-office-fluent-ribbon).

