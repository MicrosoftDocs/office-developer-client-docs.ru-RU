---
title: DeleteObject Macro Action
TOCTitle: DeleteObject Macro Action
ms:assetid: a8deb2a7-4e73-8696-b8c1-3a3939d813f7
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821415(v=office.15)
ms:contentKeyID: 48546912
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm152112
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 85e9fc888e06a69be6f458ed03ad92b8253b30a2
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25481270"
---
# <a name="deleteobject-macro-action"></a>DeleteObject Macro Action


**Применимо к**: Access 2013 | Office 2013

Действие **DeleteObject** можно использовать для удаления объекта указанной базы данных.


> [!NOTE]
> <P>
		Эта действие не разрешено, если база данных не является доверенной. Дополнительные сведения о включении макросов см. по ссылкам в разделе See Also этой статьи.
</P>



## <a name="setting"></a>Параметр

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
> <P>Если оставить поля <STRONG>Тип объекта</STRONG> и <STRONG>Имя объекта</STRONG> , Access удаляет объект, выбранного в области навигации без вывода предупреждающего сообщения при обнаружении <STRONG>DeleteObject</STRONG> действие.</P>



## <a name="remarks"></a>Замечания

Чтобы удалить временные объекты, созданные во время выполнения макроса можно использовать действие **DeleteObject** . Например можно использовать **ОткрытьЗапрос** для выполнения запроса создание таблицы, который создает временные таблицы. По окончании с помощью временной таблицы, можно использовать действие **DeleteObject** удалить ее.

Это действие имеет тот же эффект, что при выборе объекта в области навигации и затем нажав клавишу DEL или щелкнув правой кнопкой мыши объект в области навигации и выбрав команду **Удалить**.

Чтобы выполнить действие **DeleteObject** в Visual Basic для приложений модуля, можно использовать метод **DeleteObject** **объекта** .

