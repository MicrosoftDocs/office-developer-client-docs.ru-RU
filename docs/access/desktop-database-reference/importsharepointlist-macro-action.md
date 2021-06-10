---
title: Макрокоманда ImportSharePointList
TOCTitle: ImportSharePointList macro action
ms:assetid: 6a633d7d-d81d-0e2e-6c1c-706a552c1bf2
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195403(v=office.15)
ms:contentKeyID: 48545429
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm152234
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: df77d2375b66df907832b6ff2717427ae54a35a4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291861"
---
# <a name="importsharepointlist-macro-action"></a>Макрокоманда ImportSharePointList

**Область применения**: Access 2013, Office 2013

Вы можете использовать **действие ImportSharePointList** для импорта или ссылки данных с сайта Microsoft SharePoint Foundation.

> [!NOTE]
> Эта макрокоманда доступна только для доверенных баз данных. 

## <a name="setting"></a>Параметр

Действие **ImportSharePointList** имеет следующие аргументы.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Аргумент макрокоманды</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Тип преобразования</strong></p></td>
<td><p>Выберите тип переноса.</p>
<ul>
<li><p>Выберите <strong>Импорт</strong> для копирования данных SharePoint Foundation в таблицу в Microsoft Access. Обновления данных в Access не влияют на данные в SharePoint Foundation. Кроме того, обновления данных в SharePoint Foundation не влияют на данные в Access.</p></li>
<li><p>Выберите <strong>Ссылку</strong> для создания связанной таблицы в Access, которая связывается с данными в SharePoint Foundation. Обновления данных в Access отражены в SharePoint Foundation. Кроме того, обновления данных в SharePoint Foundation отражаются в Access.</p></li>
</ul>
<p></p></td>
</tr>
<tr class="even">
<td><p><strong>Адрес сайта</strong></p></td>
<td><p>Введите полный путь SharePoint сайта.</p></td>
</tr>
<tr class="odd">
<td><p><strong>ID списка</strong></p></td>
<td><p>Введите имя или GUID перенаправленного списка. Необходимый аргумент.</p></td>
</tr>
<tr class="even">
<td><p><strong>Просмотр ID</strong></p></td>
<td><p>Введите GUID представления для списка, который вы хотите использовать. Оставьте этот аргумент пустым, чтобы перенести все строки и столбцы в списке.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Имя таблицы</strong></p></td>
<td><p>Введите имя, отображаемую для таблицы или связанной таблицы в Access.</p></td>
</tr>
<tr class="even">
<td><p><strong>Получить значения отображения lookup</strong></p></td>
<td><p>Выберите <strong>Да</strong> для переноса значений отображения полей Lookup вместо ID, используемого для выполнения отображения.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Примечания

- Это действие имеет такой же эффект, как SharePoint **список** в группе **Импорт** на вкладке **Внешние** данные. Аргументы для действия соответствуют решениям, которые вы делаете в мастере внешних данных Get.

- Чтобы выполнить **действие ImportSharePointList** в модуле VBA, используйте метод **TransferSharePointList** объекта **DoCmd.**

- При указании несущестуго списка или представления ошибки не происходит и данные не передаются.

- GUID — уникальный идентификатор hexadecimal для списка или представления. GUID должен быть введен в следующем формате, где каждый "F" является гексадецимальным номером (от 0 до 9 или A через F).
    
  `{FFFFFFFF-FFFF-FFFF-FFFF-FFFFFFFFFFFF}`
    
  Вы можете получить GUID для списка или представления с сайта SharePoint с помощью следующей процедуры:
    
  1. Откройте список в SharePoint Foundation.
    
  2. Если нужное представление не отображается, щелкните стрелку **представления,** а затем выберите нужное представление.
    
  3. Щелкните **стрелку "Просмотр",** а затем выберите **Изменение этого представления.** Адрес в панели адресов браузера содержит GUID-коды как для списка, так и для представления. GUID для списка следует **List=** и GUID для представления следует **View=**. Однако в адресе каждый **символ {(левая** скобка) представлен строкой **%7B,** каждый символ (дефис) представлен строкой **-** **%2D,** а каждый **символ }** (справа скобка) представлен строкой **%7D**. Пример.
        
     `https://MySite12/_layouts/ViewEdit.aspx?List=%7B2A82A404%2D5529%2D47DC%2DAE13%2DAC1D9BC0A84F%7D&View=%7B357B4FE6%2D44CF%2D4275%2DB91F%2D46558301579B%7D`
        
  Прежде чем использовать GUID-интерфейсы из адреса в качестве аргументов в этом макросовом действии, необходимо заменить каждую строку **%7B** на **{character,** заменить каждую строку **%2D** на символ и заменить каждую **-** **строку %7D** на **}.** Не включите **&** символ (ampersand), который следует **строке %7D** в GUID списка.

