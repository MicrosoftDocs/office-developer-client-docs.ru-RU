---
title: LogEvent Macro Action
TOCTitle: LogEvent Macro Action
ms:assetid: 3578c725-64b9-385e-ef73-a15cdf751c33
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192460(v=office.15)
ms:contentKeyID: 48544148
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f626dd61782baed2e46aa931891a172fc53c1bde
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25481851"
---
# <a name="logevent-macro-action"></a>LogEvent Macro Action


**Применимо к**: Access 2013 | Office 2013

Действие **LogEvent** записывает сведения об **системы см** .


> [!NOTE]
> <P><STRONG>LogEvent</STRONG> действие доступно только в макросов данных.</P>



## <a name="setting"></a>Параметр

Действие **LogEvent** имеет следующие аргументы.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Argument</p></th>
<th><p>Обязательный</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Описание</strong></p></td>
<td><p>НЕТ</p></td>
<td><p>Строковое выражение, описывающее условие, следует регистрировать. Описание не может превышать 255 знаков.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Замечания

Действие **LogEvent** можно использовать для записи сведений о состоянии **, не никак с помощью действия **[RaiseError](raiseerror-macro-action.md)** приводит к возникновению ошибки системы см** . К примеру вы журнал изменений для определенного поля или использовать при отладке макрос с помощью элементов в **USysApplicationLog** .

При использовании **LogEvent** действие для записи **см** в столбце **категории** автоматически устанавливается значение **пользователя**.

Чтобы просмотреть **сведения см** , выполните следующие действия:

1.  Выберите в меню **файл** и выберите пункт **Параметры**.

2.  В диалоговом окне **Параметры доступа к** перейдите на вкладку **Текущей базы данных** .

3.  В разделе **Переходы** щелкните **Параметры навигации**.

4.  В диалоговом окне **Параметры навигации** нажмите кнопку **Показать системные объекты**и нажмите кнопку **ОК**.

5.  Нажмите **кнопку ОК** , чтобы закрыть диалоговое окно **Параметры доступа** .

