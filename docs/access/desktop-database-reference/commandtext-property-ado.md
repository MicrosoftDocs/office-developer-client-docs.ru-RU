---
title: CommandText Property (ADO)
TOCTitle: CommandText Property (ADO)
ms:assetid: 0debec1c-068f-0aea-fce8-e61aa39c5907
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248859(v=office.15)
ms:contentKeyID: 48543234
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- ado210.chm1231123
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 9000f069c7669872c686c013520f886d16e3619b
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25479817"
---
# <a name="commandtext-property-ado"></a>CommandText Property (ADO)


**Применимо к**: Access 2013 | Office 2013

Указывает текст команды для выдачи с использованием поставщика.

## <a name="settings-and-return-values"></a>Параметры и возвращаемые значения

Задает или возвращает **строковое** значение, содержащее команды поставщика, например инструкции SQL, имя таблицы, относительный URL-адрес или вызова хранимой процедуры. Значение по умолчанию — «» (пустая строка).

## <a name="remarks"></a>Замечания

Используйте свойство **CommandText** задает или возвращает текст команды, представленного объектом [команды](command-object-ado.md) . Обычно это будет инструкции SQL, но также может быть любой тип оператора команду распознаются поставщиком, такие как вызов хранимой процедуры. Оператор SQL должен быть определенного диалект или версия, поддерживаемая обработчик запросов поставщика.

Если свойство [подготовленных](prepared-property-ado.md) объекта **команды** имеет значение **True** , объект **команды** привязан к открытое подключение, если свойство **CommandText** ADO подготавливает запроса (то есть, скомпилированной формы запроса который хранится поставщиком) при вызове метода [Execute](https://msdn.microsoft.com/library/jj248785\(v=office.15\)) или **Open** .

В зависимости от настройки свойства [CommandType](commandtype-property-ado.md) ADO может изменить свойство **CommandText** . Свойство **CommandText** можно прочитать в любое время, чтобы увидеть текст фактические команды, ADO будет использовать во время выполнения.

Используйте свойство **CommandText** задает или возвращает относительный URL-адрес, который задает ресурс, такой как файл или папку. Ресурс является относительно местоположения, явно указаны с абсолютный URL-адрес, или неявно open объекта [подключения](connection-object-ado.md) .


> [!NOTE]
> <P>URL-адреса, с помощью схемы http автоматически вызывает <A href="microsoft-ole-db-provider-for-internet-publishing.md">Поставщик Microsoft OLE DB для публикации Интернет</A>. Для получения дополнительных сведений см <A href="absolute-and-relative-urls.md">абсолютного и относительных URL-адресов</A>.</P>


