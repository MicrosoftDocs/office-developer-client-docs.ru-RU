---
title: Макрокоманда SaveObject
TOCTitle: SaveObject macro action
ms:assetid: 85716dfc-f76f-ca47-cc40-f8f88162f85a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196789(v=office.15)
ms:contentKeyID: 48546060
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm116962
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: cf6fe02616134f864a0e07092951ab9cf49aadbc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308934"
---
# <a name="saveobject-macro-action"></a>Макрокоманда SaveObject

**Область применения**: Access 2013, Office 2013

Вы можете использовать **действие SaveObject** для сохранения указанного объекта Access или активного объекта, если его нет. Кроме того, в некоторых случаях можно сохранить активный объект с новым именем (эта функция выполняется так же, как и команда **Save As** на панели инструментов **быстрого доступа).**

> [!NOTE]
> Эта макрокоманда доступна только для доверенных баз данных. 

## <a name="setting"></a>Параметр

Действие **SaveObject** имеет следующие аргументы.

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
<td><p><strong>Object Type</strong></p></td>
<td><p>Тип объекта, который необходимо сохранить. <strong>Щелкните</strong> <strong>таблицу,</strong> <strong>запрос,</strong>форма, отчет, макрос, модуль, <strong></strong> <strong></strong>страница доступа <strong></strong> к данным, представление сервера, схема, сохраненная процедура или функция в поле Тип объекта в разделе Аргументы действий области Macro Builder. <strong></strong> <strong></strong> <strong></strong> <strong></strong> <strong></strong> <strong></strong> <strong></strong> Чтобы выбрать активный объект, оставьте этот аргумент пустым. Если в этом аргументе выбран тип объекта, необходимо выбрать имя существующего объекта в <strong>аргументе "Имя объекта".</strong></p></td>
</tr>
<tr class="even">
<td><p><strong>Object Name</strong></p></td>
<td><p>Имя объекта, который необходимо сохранить. Поле <strong>Object Name</strong> отображает все объекты базы данных, относящиеся к типу, заданному аргументом <strong>Object Type</strong>. Если оставить аргумент <strong>Object Type</strong> пустым, этот аргумент можно оставить пустым, чтобы сохранить активный объект, или, в некоторых случаях, ввести новое имя в этом аргументе, чтобы сохранить активный объект с этим именем. Если вы вводите новое имя, имя должно следовать стандартным соглашениям именования для объектов Microsoft Access.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Примечания

Действие **SaveObject** работает на всех объектах базы данных, которые пользователь может открыто открыть и сохранить. Указанный объект должен быть открыт, чтобы действие **SaveObject** как-то сказывается на объекте. Это действие имеет тот же эффект, что и выбор объекта, а затем его сохранение, нажав **кнопку Сохранить** на панели инструментов **быстрого доступа**. 

Оставление аргумента **Object Type** пустым и ввод нового имени в аргументе **"Имя** объекта" имеет такой же эффект, как нажатие кнопки **Сохранить** как на панели инструментов быстрого доступа **и** ввод нового имени для активного объекта. Использование действия **SaveObject** позволяет указать объект для сохранения и выполнить команду **Сохранить как** из макроса.

> [!NOTE]
> Вы не можете использовать действие **SaveObject,** чтобы сохранить любое из следующих действий с новым именем:
> - Форма в представлении формы или представлении таблицы данных
> - Отчет в предварительной версии печати
> - Модуль
> - Представление сервера в представлении таблицы данных или предварительный просмотр печати
> - Страница доступа к данным в представлении Page
> - Таблица в представлении таблицы данных или предварительный просмотр печати
> - Запрос в представлении таблицы данных или предварительном просмотре печати
> - Сохраненная процедура в представлении таблицы данных или предварительном просмотре печати

Действие **SaveObject,** выполнено ли оно в макросах текущей базы данных или в базе данных библиотеки, всегда сохраняет указанный объект или активный объект в базе данных, в которой был создан объект.

Если вы сохраните активный объект с новым именем, но имя такое же, как имя существующего объекта этого типа, диалоговое окно задает вопрос, хотите ли вы перезаписать существующий объект. Если для аргумента  действия **SetWarnings** заочно установлено предупреждение, диалоговое окно не отображается, а старый объект автоматически перезаписывается.

Чтобы выполнить **действие SaveObject** в Visual Basic для приложений (VBA), используйте метод **Сохранить** объект **DoCmd.**

