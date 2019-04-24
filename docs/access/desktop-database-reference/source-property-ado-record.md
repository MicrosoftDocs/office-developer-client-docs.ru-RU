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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314555"
---
# <a name="source-property-ado-record"></a>Свойство Source (объект Record в ADO)


**Область применения**: Access 2013, Office 2013

Указывает источник данных или объект, представленный [записью](record-object-ado.md).

## <a name="settings-and-return-values"></a>Параметры и возвращаемые значения

Задает или возвращает значение **типа Variant** , которое указывает объект, представленный **записью**.

## <a name="remarks"></a>Замечания

Свойство **Source** возвращает аргумент *Source* метода [Open](open-method-ado-record.md) объекта **Record** . Он может содержать абсолютную или относительную строку URL-адреса. Абсолютный URL-адрес можно использовать без задания свойства [ActiveConnection](activeconnection-property-ado.md) для непосредственного открытия объекта **Record** . В этом случае создается объект неявного **подключения** .

Свойство **Source** также может содержать ссылку на уже открытый **набор записей**, который открывает объект **Record** , представляющий текущую строку в **наборе записей**.

Свойство **Source** также может содержать ссылку на объект [Command](command-object-ado.md) , который возвращает одну строку данных от поставщика.

Если свойство **ActiveConnection** также задано, свойство **Source** должно указать на объект, который существует в области этого подключения. Например, если свойство **Source** содержит АБСОЛЮТный URL-адрес в пространствах имен, структурированных с помощью дерева, он должен указать узел, который находится внутри области узла, определенного URL-адресом в строке подключения. Если свойство **Source** содержит отНОСИТЕЛЬНЫЙ URL-адрес, он проверяется в контексте, заданном свойством **ActiveConnection** .

Свойство **Source** доступно для чтения и записи, когда объект **Record** закрыт и доступен только для чтения, пока открыт объект **Record** .

> [!NOTE]
> URL-адреса, использующие схему HTTP, автоматически будут вызывать [поставщик Microsoft OLE DB для публикации в Интернете](microsoft-ole-db-provider-for-internet-publishing.md). Для получения дополнительных сведений см [абсолютные и относительНые URL-адреса](absolute-and-relative-urls.md).


