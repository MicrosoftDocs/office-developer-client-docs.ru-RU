---
title: Макрокоманда CloseWindow
TOCTitle: CloseWindow macro action
ms:assetid: ba96bc26-7f3f-fd3d-8d3a-e18bfe90cdf0
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822510(v=office.15)
ms:contentKeyID: 48547377
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm64319
f1_categories:
- Office.Version=v15
ms.openlocfilehash: f9bffbd129d8fb4fc1334dbd884556d98e7f140c
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25929323"
---
# <a name="closewindow-macro-action"></a>Макрокоманда CloseWindow


**Применимо к**: Access 2013, Office 2013

Действие **CloseWindow** можно использовать для закрытия указанного вкладку документ Access или активный документ, если он не задан.

## <a name="setting"></a>Параметр

Действие **CloseWindow** состоит из следующих аргументов.

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
<td><p>Тип объекта, вкладку документа, которую нужно закрыть. Выберите <strong>таблицы</strong>, <strong>запроса</strong>, <strong>формы</strong>, <strong>отчета</strong>, <strong>макрос</strong>, <strong>модуль</strong>, <strong>страницы доступа к данным</strong>, <strong>представление</strong>, <strong>Схема</strong>, <strong>хранимая процедура</strong>или <strong>функции</strong> в тип объекта <strong> </strong>флажок в разделе <strong>Действие аргументы</strong> области построения макросов. Выберите вкладку активный документ, оставьте данный аргумент пустым.</p>

> [!NOTE]
> При закрытии модуля в редакторе Visual Basic, необходимо использовать **модуль** в аргументе **Тип объекта** .


<p></p></td>
</tr>
<tr class="even">
<td><p><strong>Имя объекта</strong></p></td>
<td><p>Имя возвращаемого объекта будет закрыто. В поле <strong>Имя объекта</strong> содержит все объекты базы данных, указанному в аргументе <strong>Тип объекта</strong> типа. Щелкните объект, чтобы закрыть. Если <strong>Тип объекта</strong> аргумента оставлено пустым, оставьте аргумент пустым.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Save</strong></p></td>
<td><p>Следует ли сохранить изменения в объекте при ее закрытии. Нажмите кнопку <strong>Yes</strong> (Сохранить объект), <strong>No</strong> (закрытия объекта без сохранения), и не <strong>запрашивать пользователя</strong> (запрашивать у пользователя ли сохранить объект). Значение по умолчанию — <strong>приглашения</strong>.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Примечания

Действие **CloseWindow** работает на все объекты базы данных, которые пользователь может явно открыть или закрыть. Это действие имеет тот же эффект, как при выборе объекта и закрывая его, щелкнув правой кнопкой мыши вкладку документа объекта и затем нажмите кнопку **Закрыть** в контекстном меню или нажав кнопку **Закрыть** для объекта.

Если аргумент **Сохранить** задано значение **запроса** и объект не был сохранен перед выполняемые действия **CloseWindow** , диалоговое окно предлагать пользователю сохранить объект макрос закрывает его. Если выбрать **В** аргументе действие **УстановитьСообщения** **Нет**диалоговое окно не отображается и объект автоматически сохраняются.

Чтобы выполнить действие **CloseWindow** в Visual Basic для приложений (VBA) модуль, используйте метод **CloseWindow** **объекта** .

