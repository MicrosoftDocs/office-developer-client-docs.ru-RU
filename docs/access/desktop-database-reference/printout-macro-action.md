---
title: Макрокоманда PrintOut
TOCTitle: PrintOut macro action
ms:assetid: 13688158-1cf1-4b2e-d90a-271c8890e413
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845432(v=office.15)
ms:contentKeyID: 48543368
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm1697
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 04212a8bf63d5039c6548463612f006f0d116229
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301409"
---
# <a name="printout-macro-action"></a>Макрокоманда PrintOut

**Область применения**: Access 2013, Office 2013

Действие **PrintOut** можно использовать для печати активного объекта в открытой базе данных. Можно распечатать таблицы данных, отчеты, формы, страницы доступа к данным и модули.

> [!NOTE]
> Эта макрокоманда доступна только для доверенных баз данных. 

## <a name="setting"></a>Параметр

Действие **PrintOut** имеет следующие аргументы.

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
<td><p><strong>Диапазон печати</strong></p></td>
<td><p>Диапазон для печати. Щелкните Все <strong>(пользователь</strong> может распечатать все объекты), <strong>Selection</strong> (пользователь может распечатать выбранную часть объекта) или Страницы <strong>(пользователь</strong> может указать диапазон страниц в <strong></strong> разделе <strong>Page From</strong> and <strong>Page To</strong> arguments) в поле Диапазон печати в разделе <strong>Аргументы</strong> действий в области Macro Builder. По умолчанию <strong>все</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong>Страница Из</strong></p></td>
<td><p>Первая страница для печати. Печать начинается в верхней части этой страницы. Этот аргумент необходим, если вы выбираете <strong>Страницы в</strong> поле <strong>Диапазон печати.</strong></p></td>
</tr>
<tr class="odd">
<td><p><strong>Page To</strong></p></td>
<td><p>Последняя страница для печати. Печать останавливается в нижней части этой страницы. Этот аргумент необходим, если вы выбираете <strong>Страницы в</strong> поле <strong>Диапазон печати.</strong></p></td>
</tr>
<tr class="even">
<td><p><strong>Качество печати</strong></p></td>
<td><p>Качество печати. Нажмите <strong>кнопку</strong> <strong>Высокая, Средняя,</strong> <strong>Низкая</strong>или <strong>Черновик</strong>. Чем ниже качество, тем быстрее объект печатается. По умолчанию <strong>значение High</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Copies</strong></p></td>
<td><p>Количество копий для печати. По умолчанию используется значение 1.</p></td>
</tr>
<tr class="even">
<td><p><strong>Collate Copies</strong></p></td>
<td><p>Нажмите <strong>кнопку Да</strong> (соените печатные копии) или <strong>Нет</strong> (не скопировать копии). Объект может печататься быстрее, если этот аргумент заданной <strong>для No</strong>. По умолчанию — <strong>Да.</strong></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Примечания

Это действие аналогично выбору объекта, нажатию вкладки **Файл** и затем нажатию **печати**. Однако при этом действии диалоговое окно **Print** не отображается.

> [!TIP]
> Если у вас есть определенные параметры печати, которые вы часто используете, создайте макрос, содержащий действие **PrintOut** с этими настройками в своих аргументах.

Аргументы для этого действия соответствуют параметрам в диалоговом окне **Печать.** Однако, в отличие от **действия FindRecord** и диалоговое окно FindRecord и **Find and Replace,** параметры аргументов не разделяются с вариантами диалоговых полей **Print.**

Чтобы выполнить действие **PrintOut** в Visual Basic для приложений (VBA), используйте метод **PrintOut** объекта **DoCmd.**

