---
title: Свойство Source (объект Record в ADO)
TOCTitle: Source property (ADO Record)
ms:assetid: f36f0f5f-4493-d8c5-db4b-c72f5031bcb3
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250235(v=office.15)
ms:contentKeyID: 48548670
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9bd1e1259eb7b089d0387dd385ee5157eeac2f34
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28698738"
---
# <a name="source-property-ado-record"></a>Свойство Source (объект Record в ADO)


**Применимо к**: Access 2013, Office 2013

Указывает источник данных или объектов, представленных в [записи](record-object-ado.md).

## <a name="settings-and-return-values"></a>Параметры и возвращаемые значения

Задает или возвращает значение **типа Variant** , которое указывает, сущности, представленной **записи**.

## <a name="remarks"></a>Замечания

Свойство **Source** возвращает *исходный* аргумент методу [Open](open-method-ado-record.md) объекта **записи** . Он может содержать абсолютное или относительное строку URL-адреса. Абсолютный URL-адрес может использоваться без установки свойства [ActiveConnection](activeconnection-property-ado.md) непосредственно открыть объект **записи** . В этом случае создается объект **подключения** неявных.

Свойство **Source** также может содержать ссылки на уже открытой **записей**, открывающий **записи** объект, представляющий текущую строку в **набора записей**.

Свойство **Source** может также содержать ссылку на объект [команды](command-object-ado.md) , который возвращает одну строку данных от поставщика.

Если задано свойство **ActiveConnection** , свойство **Source** должен указывать некоторые объект, который существует в пределах это подключение. Например в пространствах имен структура дерева, если свойство **Source** содержит абсолютный URL-адрес оно должно указывать на узел, который существует внутри области узла, определяемую средством URL-адрес в строку подключения. Если свойство **Source** содержит относительный URL-адрес, он проверяется в контексте, заданной свойством **ActiveConnection** .

Свойство **Source** — чтение и запись во время объект **записи** закрывается и доступен только для чтения, когда объект **записи** открыт.

> [!NOTE]
> URL-адреса, с помощью схемы http автоматически вызывает [Поставщик Microsoft OLE DB для публикации Интернет](microsoft-ole-db-provider-for-internet-publishing.md). Для получения дополнительных сведений см [абсолютных и относительных URL-адресов](absolute-and-relative-urls.md).


