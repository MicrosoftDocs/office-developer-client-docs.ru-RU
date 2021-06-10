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

Указывает текст команды, которая будет выдана поставщику.

## <a name="settings-and-return-values"></a>Параметры и значения возврата

Задает или возвращает значение **String,** содержаное команду поставщика, например SQL, имя таблицы, относительный URL-адрес или вызов сохраненной процедуры. По умолчанию — строка "" (строка нулевой длины).

## <a name="remarks"></a>Примечания

Используйте свойство **CommandText** для набора или возврата текста команды, представленной объектом [Command.](command-object-ado.md) Обычно это будет SQL, но может быть и любой другой тип командного оператора, распознаемого поставщиком, например вызов сохраненной процедуры. Оператор SQL должен быть определенного диалекта или версии, поддерживаемой обработчиком запросов поставщика.

Если [](prepared-property-ado.md) свойство Prepared объекта **Command** настроено на **True,** а объект **Command** привязан к открытому подключению при задавате свойства **CommandText,** ADO готовит запрос (т. е. компилировать форму запроса, хранимого поставщиком) при вызове методов [Выполнить](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command) или **Открыть.**

В зависимости от параметра [свойства CommandType](commandtype-property-ado.md) ADO может изменять **свойство CommandText.** Вы можете прочитать свойство **CommandText** в любое время, чтобы увидеть фактический текст команды, который будет использовать ADO во время выполнения.

Используйте свойство **CommandText,** чтобы установить или вернуть относительный URL-адрес, который указывает ресурс, например файл или каталог. Ресурс имеет отношение к расположению, явно указанному абсолютным URL-адресом или неявным образом объектом open [Connection.](connection-object-ado.md)


> [!NOTE]
> URL-адреса, использующие схему http, автоматически вызывают поставщика DB Microsoft [OLE для публикации в Интернете.](microsoft-ole-db-provider-for-internet-publishing.md) Дополнительные сведения см. в [url-адресах Absolute и relative.](absolute-and-relative-urls.md)


