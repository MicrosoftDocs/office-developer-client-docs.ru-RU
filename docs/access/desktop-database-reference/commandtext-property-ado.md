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

Указывает текст команды, которая будет выдаваться поставщику.

## <a name="settings-and-return-values"></a>Параметры и возвращаемые значения

Задает или возвращает **строковое** значение, содержащее команду поставщика, например инструкцию SQL, имя таблицы, отНОСИТЕЛЬНЫЙ URL-адрес или вызов хранимой процедуры. Значение по умолчанию "" (строка нулевой длины).

## <a name="remarks"></a>Замечания

Используйте свойство **CommandText** , чтобы задать или вернуть текст команды, представленной объектом [Command](command-object-ado.md) . Как правило, это инструкция SQL, но она также может быть любым другим типом командного оператора, распознаваемым поставщиком, например вызовом хранимой процедуры. Инструкция SQL должна относиться к определенному диалекту или версии, поддерживаемой обработчиком запросов поставщика.

Если для свойства [Prepared](prepared-property-ado.md) объекта **Command** задано значение **true** , а объект **Command** привязан к открытому подключению, когда вы задаете свойство **CommandText** , ADO подготавливает запрос (то есть скомпилированную форму запроса). , хранящийся у поставщика) при вызове методов [EXECUTE](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command) и **Open** .

В зависимости от значения свойства [CommandType](commandtype-property-ado.md) , ADO может изменить свойство **CommandText** . В любой момент можно прочитать свойство **CommandText** , чтобы увидеть текст команды, который будет использоваться ADO во время выполнения.

Используйте свойство **CommandText** , чтобы задать или вернуть отНОСИТЕЛЬНЫЙ URL-адрес, указывающий ресурс, например файл или каталог. Ресурс относительный относительно расположения, указанного абсолютным URL-АДРЕСом, или неявно с помощью объекта открытого [подключения](connection-object-ado.md) .


> [!NOTE]
> URL-адреса, использующие схему HTTP, автоматически будут вызывать [поставщик Microsoft OLE DB для публикации в Интернете](microsoft-ole-db-provider-for-internet-publishing.md). Для получения дополнительных сведений см [абсолютные и относительНые URL-адреса](absolute-and-relative-urls.md).


