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
ms.openlocfilehash: 86f69be8ed9216619f10bc70e2c701fb109d0ff5
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25879307"
---
# <a name="commandtext-property-ado"></a>Свойство CommandText (ADO)


**Применимо к**: Access 2013, Office 2013

Указывает текст команды для выдачи с использованием поставщика.

## <a name="settings-and-return-values"></a>Параметры и возвращаемые значения

Задает или возвращает **строковое** значение, содержащее команды поставщика, например инструкции SQL, имя таблицы, относительный URL-адрес или вызова хранимой процедуры. Значение по умолчанию — «» (пустая строка).

## <a name="remarks"></a>Замечания

Используйте свойство **CommandText** задает или возвращает текст команды, представленного объектом [команды](command-object-ado.md) . Обычно это будет инструкции SQL, но также может быть любой тип оператора команду распознаются поставщиком, такие как вызов хранимой процедуры. Оператор SQL должен быть определенного диалект или версия, поддерживаемая обработчик запросов поставщика.

Если свойство [подготовленных](prepared-property-ado.md) объекта **команды** имеет значение **True** , объект **команды** привязан к открытое подключение, если свойство **CommandText** ADO подготавливает запроса (то есть, скомпилированной формы запроса который хранится поставщиком) при вызове метода [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command) или **Open** .

В зависимости от настройки свойства [CommandType](commandtype-property-ado.md) ADO может изменить свойство **CommandText** . Свойство **CommandText** можно прочитать в любое время, чтобы увидеть текст фактические команды, ADO будет использовать во время выполнения.

Используйте свойство **CommandText** задает или возвращает относительный URL-адрес, который задает ресурс, такой как файл или папку. Ресурс является относительно местоположения, явно указаны с абсолютный URL-адрес, или неявно open объекта [подключения](connection-object-ado.md) .


> [!NOTE]
> URL-адреса, с помощью схемы http автоматически вызывает [Поставщик Microsoft OLE DB для публикации Интернет](microsoft-ole-db-provider-for-internet-publishing.md). Для получения дополнительных сведений см [абсолютных и относительных URL-адресов](absolute-and-relative-urls.md).


