---
title: Макрокоманда DeleteObject
TOCTitle: DeleteObject macro action
ms:assetid: a8deb2a7-4e73-8696-b8c1-3a3939d813f7
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821415(v=office.15)
ms:contentKeyID: 48546912
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm152112
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: dae5718e7b4cb609cb50bd65ee6e2486f4ebaab6
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28700096"
---
# <a name="deleteobject-macro-action"></a>Макрокоманда DeleteObject

**Применимо к**: Access 2013, Office 2013

Действие **DeleteObject** можно использовать для удаления объекта указанной базы данных.

> [!NOTE]
> Это действие не разрешено, если база данных не является доверенной. 

## <a name="setting"></a>Setting

Действие **DeleteObject** имеет следующие аргументы.

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
<td><p><strong>Тип объекта</strong></p></td>
<td><p>Тип объекта для удаления. Выберите <strong>таблицы</strong>, <strong>запроса</strong>, <strong>формы</strong>, <strong>отчета</strong>, <strong>макрос</strong>, <strong>модуль</strong>, <strong>страницы доступа к данным</strong>, <strong>представление</strong>, <strong>Схема</strong>, <strong>хранимая процедура</strong>или <strong>функции</strong> в тип объекта <strong> </strong>флажок в разделе <strong>Действие аргументы</strong> области построения макросов. Для удаления объекта, выделенного в области навигации, оставьте аргумент пустым.</p></td>
</tr>
<tr class="even">
<td><p><strong>Имя объекта</strong></p></td>
<td><p>Имя объекта для удаления. В поле <strong>Имя объекта</strong> содержит все объекты базы данных, указанному в аргументе <strong>Тип объекта</strong> типа. Если в поле <strong>Тип объекта</strong> оставить пустым, оставьте это поле пустым. Если макрос, содержащий <strong>DeleteObject</strong> действие в базе данных библиотеки, Microsoft Office Access 2007 сначала выполняет поиск объекта с указанным именем в базе данных библиотеки, а затем в текущей базе данных.</p></td>
</tr>
</tbody>
</table>

> [!WARNING]
> Если оставить поля **Тип объекта** и **Имя объекта** , Access удаляет объект, выбранного в области навигации без вывода предупреждающего сообщения при обнаружении **DeleteObject** действие.

## <a name="remarks"></a>Замечания

Чтобы удалить временные объекты, созданные во время выполнения макроса можно использовать действие **DeleteObject** . Например можно использовать **ОткрытьЗапрос** для выполнения запроса создание таблицы, который создает временные таблицы. По окончании с помощью временной таблицы, можно использовать действие **DeleteObject** удалить ее.

Это действие имеет тот же эффект, что при выборе объекта в области навигации и затем нажав клавишу DEL или щелкнув правой кнопкой мыши объект в области навигации и выбрав команду **Удалить**.

Чтобы выполнить действие **DeleteObject** в Visual Basic для приложений модуля, можно использовать метод **DeleteObject** **объекта** .

