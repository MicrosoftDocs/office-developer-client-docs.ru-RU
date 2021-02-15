---
title: Свойство CommandText (ADO)
TOCTitle: CommandText property (ADO)
ms:assetid: 0debec1c-068f-0aea-fce8-e61aa39c5907
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248859(v=office.15)
ms:contentKeyID: 48543234
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- ado210.chm1231123
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 66797accb24cead7d7ba5732f0a9c58ee31049e5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296138"
---
# <a name="commandtext-property-ado"></a>Свойство CommandText (ADO)


**Область применения**: Access 2013, Office 2013

Указывает текст команды, которая должна быть выдана поставщику.

## <a name="settings-and-return-values"></a>Параметры и возвращаемые значения

Задает или возвращает **строку,** содержаную команду поставщика, например оператор SQL, имя таблицы, относительный URL-адрес или хранимый вызов процедуры. Значение по умолчанию: "" (строка нулевой длины).

## <a name="remarks"></a>Заметки

Используйте свойство **CommandText,** чтобы установить или вернуть текст команды, представленной [объектом Command.](command-object-ado.md) Обычно это оператор SQL, но также может быть любым другим типом оператора команды, распознаемого поставщиком, например вызовом хранимой процедуры. Оператор SQL должен иметь определенный диалект или версию, поддерживаемую обработчиком запросов поставщика.

Если свойство [Prepared](prepared-property-ado.md) объекта **Command** имеет свойство **True** и объект **Command** привязываться к открытому подключению при выполнении свойства **CommandText,** ADO подготавливает запрос (т. е. скомпилную форму запроса, который хранится поставщиком) при вызове методов [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command) или **Open.**

В зависимости от [параметра свойства CommandType](commandtype-property-ado.md) ADO может изменить **свойство CommandText.** Вы можете прочитать свойство **CommandText** в любое время, чтобы увидеть фактический текст команды, который ADO будет использовать во время выполнения.

Используйте свойство **CommandText,** чтобы установить или вернуть относительный URL-адрес, который указывает ресурс, например файл или каталог. Ресурс является относительным расположением, явным образом указанным абсолютным URL-адресом, или неявно открытым [объектом Connection.](connection-object-ado.md)


> [!NOTE]
> URL-адреса, использующие схему HTTP, автоматически вызывают поставщика [Microsoft OLE DB для интернет-публикации.](microsoft-ole-db-provider-for-internet-publishing.md) Дополнительные сведения см. в [сведениях об абсолютных и относительных URL-адресах.](absolute-and-relative-urls.md)


