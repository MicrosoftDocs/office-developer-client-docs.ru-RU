---
title: Скрытие ленты при запуске Access
TOCTitle: Hide the ribbon when Access starts
description: Узнайте, как загрузить в Access 2013 настроенную ленту, на которой скрыты все встроенные вкладки.
ms:assetid: f98bab58-8094-1c56-f70b-ced2e7849574
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837012(v=office.15)
ms:contentKeyID: 48548817
ms.date: 10/16/2018
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: 384a575ae5e15b75ba7b0b891529c695cc3de599
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34537831"
---
# <a name="hide-the-ribbon-when-access-starts"></a>Скрытие ленты при запуске Access

**Область применения**: Access 2013 | Office 2013

По умолчанию Microsoft Access не предоставляет метод для скрытия ленты. В этой статье описывается, как загрузить пользовательскую ленту, на которой скрыты все встроенные вкладки.

Чтобы загрузить пользовательскую ленту при запуске Access, необходимо сохранить ее параметры в таблице с именем **USysRibbons**.

Таблицу **USysRibbons** необходимо создать с использованием конкретных имен столбцов для реализуемых настроек ленты. 

В приведенной ниже таблице перечислены параметры, используемые при создании таблицы **USysRibbons**.

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
<td><p>Содержит имя пользовательской ленты, которая будет связана с этой настройкой.</p></td>
</tr>
<tr class="even">
<td><p><strong>RibbonXML</strong></p></td>
<td><p>Заметка</p></td>
<td><p>Содержит код XML для расширения ленты (RibbonX), определяющий настройку ленты.</p></td>
</tr>
</tbody>
</table>

<br/>

В приведенной ниже таблице перечислены параметры для настройки ленты, которые будут храниться в таблице **USysRibbons**.

|Имя столбца|Значение|
|:----------|:----|
|**RibbonName**|HideTheRibbon|
|**RibbonXML**|`<CustomUI xmlns="http://schemas.microsoft.com/office/2006/01/CustomUI"> <ribbon startFromScratch="true"/></CustomUI>`|


## <a name="apply-a-custom-ribbon-when-access-starts"></a>Применение пользовательской ленты при запуске Access

Чтобы применить пользовательскую ленту, которая будет доступна при запуске приложения, используйте описанную ниже процедуру.

1.  Выполните описанные выше действия, чтобы сделать настроенную ленту доступной приложению.

2.  Закройте и перезапустите приложение.

3.  Нажмите **кнопку Microsoft Office**![O12FileMenuButton\_ZA10077102](media/access-file-menu-button.gif "O12FileMenuButton_ZA10077102") и выберите пункт **Параметры Access**.

4.  Выберите вариант **Текущая база данных**, а затем в разделе **Параметры ленты и панелей инструментов** выберите список **Имя ленты** и нажмите **HideTheRibbon**.

5.  Закройте и перезапустите приложение.

> [!NOTE]
> Дополнительные сведения о пользовательском интерфейсе ленты в других приложениях Office см. в статье [Обзор ленты Office Fluent](https://docs.microsoft.com/office/vba/Library-Reference/Concepts/overview-of-the-office-fluent-ribbon).


