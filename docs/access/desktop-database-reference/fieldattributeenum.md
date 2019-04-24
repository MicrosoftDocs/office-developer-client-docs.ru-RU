---
title: Фиелдаттрибутинум (Справочник по базам данных Access на компьютере)
TOCTitle: FieldAttributeEnum
ms:assetid: 2d3a541e-a437-6108-ab0e-90c7884b3df7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249071(v=office.15)
ms:contentKeyID: 48543967
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 079c79af3d15a6a5864a7db7f8334393258cfd42
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292603"
---
# <a name="fieldattributeenum"></a>FieldAttributeEnum

**Область применения**: Access 2013, Office 2013

Задает один или несколько атрибутов объекта [field](field-object-ado.md) .

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Константа</p></th>
<th><p>Значение</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Адфлдкачедеферред</strong></p></td>
<td><p>0x1000</p></td>
<td><p>Указывает, что поставщик кэширует значения полей, а последующие операции чтения выполняются из кэша.</p></td>
</tr>
<tr class="even">
<td><p><strong>Адфлдфиксед</strong></p></td>
<td><p>0x10</p></td>
<td><p>Указывает, что поле содержит данные фиксированной длины.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Адфлдисчаптер</strong></p></td>
<td><p>0x2000</p></td>
<td><p>Указывает, что поле содержит значение главы, которое указывает конкретный дочерний набор записей, связанный с этим родительским полем. Обычно поля главы используются с формированием данных или фильтрами.</p></td>
</tr>
<tr class="even">
<td><p><strong>Адфлдисколлектион</strong></p></td>
<td><p>0x40000</p></td>
<td><p>Указывает, что поле указывает, что ресурс, представленный записью, является коллекцией других ресурсов, например папки, а не простым ресурсом, например текстовым файлом.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Адфлдисдефаултстреам</strong></p></td>
<td><p>0x20000</p></td>
<td><p>Указывает, что поле содержит поток по умолчанию для ресурса, представленного записью. Например, поток по умолчанию может быть HTML-контентом корневой папки на веб-сайте, который автоматически обрабатывается, когда указан корневой URL-адрес.</p></td>
</tr>
<tr class="even">
<td><p><strong>Адфлдиснуллабле</strong></p></td>
<td><p>0x20</p></td>
<td><p>Указывает, что поле принимает значения NULL.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Адфлдисровурл</strong></p></td>
<td><p>0x10000</p></td>
<td><p>Указывает, что поле содержит URL-адрес, указывающий ресурс из хранилища данных, представленного записью.</p></td>
</tr>
<tr class="even">
<td><p><strong>Адфлдлонг</strong></p></td>
<td><p>0x80</p></td>
<td><p>Указывает, что поле является длинным бинарным полем. Также указывает, что вы можете использовать методы AppendChunk <a href="getchunk-method-ado.md"></a> и <a href="appendchunk-method-ado.md"></a> .</p></td>
</tr>
<tr class="odd">
<td><p><strong>Адфлдмайбенулл</strong></p></td>
<td><p>0x40</p></td>
<td><p>Указывает, что в поле можно считывать значения NULL.</p></td>
</tr>
<tr class="even">
<td><p><strong>Адфлдмайдефер</strong></p></td>
<td><p>0x2</p></td>
<td><p>Указывает, что поле является отложенным — то есть значения полей не извлекаются из источника данных с использованием всей записи, но только при явном доступе к ним.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Адфлднегативескале</strong></p></td>
<td><p>0x4000</p></td>
<td><p>Указывает, что поле представляет числовое значение из столбца, поддерживающего отрицательные значения шкалы. Масштаб задается свойством <a href="numericscale-property-ado.md">NumericScale</a> .</p></td>
</tr>
<tr class="even">
<td><p><strong>Адфлдровид</strong></p></td>
<td><p>0x100</p></td>
<td><p>Указывает, что поле содержит постоянный идентификатор строки, который не может быть записан в и имеет неосмысленное значение, за исключением идентификации строки (например, номера записи, уникального идентификатора и т. д.).</p></td>
</tr>
<tr class="odd">
<td><p><strong>Адфлдровверсион</strong></p></td>
<td><p>0x200</p></td>
<td><p>Указывает, что поле содержит дату и время, которые используются для отслеживания обновлений.</p></td>
</tr>
<tr class="even">
<td><p><strong>Адфлдункновнупдатабле</strong></p></td>
<td><p>0x8</p></td>
<td><p>Указывает, что поставщик не может определить, можно ли выполнять запись в поле.</p></td>
</tr>
<tr class="odd">
<td><p><strong>АдфлдунспеЦифиед</strong></p></td>
<td><p>–1<br />
Равен</p></td>
<td><p>Указывает, что поставщик не задает атрибуты поля.</p></td>
</tr>
<tr class="even">
<td><p><strong>Адфлдупдатабле</strong></p></td>
<td><p>0x4</p></td>
<td><p>Указывает, что вы можете выполнять запись в поле.</p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a>Эквивалент ADO/WFC

Пакет: **com. MS. WFC. Data**

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Константа</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Адоенумс. Фиелдаттрибуте. КАЧЕДЕФЕРРЕД</p></td>
</tr>
<tr class="even">
<td><p>Адоенумс. Фиелдаттрибуте. FIXED</p></td>
</tr>
<tr class="odd">
<td><p>Адоенумс. Фиелдаттрибуте. NULL</p></td>
</tr>
<tr class="even">
<td><p>Адоенумс. Фиелдаттрибуте. LONG</p></td>
</tr>
<tr class="odd">
<td><p>Адоенумс. Фиелдаттрибуте. МАЙБЕНУЛЛ</p></td>
</tr>
<tr class="even">
<td><p>Адоенумс. Фиелдаттрибуте. МАЙДЕФЕР</p></td>
</tr>
<tr class="odd">
<td><p>Адоенумс. Фиелдаттрибуте. НЕГАТИВЕСКАЛЕ</p></td>
</tr>
<tr class="even">
<td><p>Адоенумс. Фиелдаттрибуте. ROWID</p></td>
</tr>
<tr class="odd">
<td><p>Адоенумс. Фиелдаттрибуте. ROWVERSION</p></td>
</tr>
<tr class="even">
<td><p>Адоенумс. Фиелдаттрибуте. УНКНОВНУПДАТАБЛЕ</p></td>
</tr>
<tr class="odd">
<td><p>Адоенумс. Фиелдаттрибуте. unspecifieded</p></td>
</tr>
<tr class="even">
<td><p>Адоенумс. Фиелдаттрибуте. ОБНОВЛЯЕМый</p></td>
</tr>
</tbody>
</table>

