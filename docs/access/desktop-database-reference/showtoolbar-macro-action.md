---
title: ShowToolbar Macro Action
TOCTitle: ShowToolbar Macro Action
ms:assetid: 9e53009b-1e5e-1bee-3bcc-f82dc1b0dc48
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198288(v=office.15)
ms:contentKeyID: 48546649
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm27417
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 462dbd34f5666643cceff1fc96b9dd77c36d0071
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25481224"
---
# <a name="showtoolbar-macro-action"></a>ShowToolbar Macro Action


**Применимо к**: Access 2013 | Office 2013

**ПанельИнструментов** можно использовать для отображения или скрытия группы команд на вкладке **Надстройки** .


> [!NOTE]
> <P><STRONG>ПанельИнструментов</STRONG> не влияет на контекстные меню.</P>




> [!NOTE]
> <P>
		Эта действие не разрешено, если база данных не является доверенной. Дополнительные сведения о включении макросов см. по ссылкам в разделе See Also этой статьи.
</P>



## <a name="setting"></a>Параметр

**ПанельИнструментов** имеет следующие аргументы.

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
<td><p><strong>Имя панели инструментов</strong></p></td>
<td><p>Имя группы команд на вкладке <strong>Надстройки</strong> требуется отобразить или скрыть. В поле <strong>Имя панели инструментов</strong> в разделе <strong>Действие аргументы</strong> области конструктор макросов показаны все доступные группы, которые могут повлиять это действие. Обязательный аргумент. Если макрос, содержащий <strong>ПанельИнструментов в базе данных библиотеки</strong> , сначала поиск группу с этим именем в базе данных библиотеки, а затем в текущей базе данных.</p></td>
</tr>
<tr class="even">
<td><p><strong>Show</strong> (Отображение)</p></td>
<td><p>Указывает на отображение или скрытие группы и в представлений для отображения или скрытия его. Значение по умолчанию — <strong>Да</strong> (Показать группы в любое время). <strong>Да,</strong> можно выбрать для отображения в группу на всех время, <strong>Где соответствующие</strong> для отображения в группу только в том случае, если соответствующий форму или отчет является активным, или <strong>не</strong> для скрытия группы в любое время.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Замечания

Это действие можно использовать в макросе с условного выражения для отображения или скрытия группы в зависимости от определенных условий.

Если вы хотите отобразить определенную группу на форме или отчета, свойству **OnActivate** форму или отчет можно присвоить имя макроса, содержащего **ПанельИнструментов для отображения группы** . Имя макроса, содержащего **ПанельИнструментов, чтобы скрыть группу** установите свойство **OnDeactivate** форму или отчет.

Встроенные панели инструментов, недоступны для отображения или скрытия с помощью этого действия, если свойству **AllowBuiltInToolbars** присвоено значение **False** (0 в Visual Basic для приложений (VBA) модуля) или установить параметр **Встроенные панели инструментов** **Значение false** в VBA с помощью метода **SetOption** .

Чтобы запустить **ПанельИнструментов** в модуль VBA, используйте метод **ПанельИнструментов** **объекта** .
