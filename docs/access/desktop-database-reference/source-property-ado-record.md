---
title: Source Property (ADO Record)
TOCTitle: Source Property (ADO Record)
ms:assetid: f36f0f5f-4493-d8c5-db4b-c72f5031bcb3
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250235(v=office.15)
ms:contentKeyID: 48548670
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4d6e010ce8db93baaf8faddaeff5ab4dabda6a84
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/17/2018
ms.locfileid: "25603387"
---
# <a name="source-property-ado-record"></a>Source Property (ADO Record)


**Применимо к**: Access 2013 | Office 2013

Указывает источник данных или объектов, представленных в [записи](record-object-ado.md).

<<<<<<< HEAD
## <a name="settings-and-return-values"></a>Параметры и возвращаемые значения
=======
## <a name="settings-and-return-values"></a>Параметры и возвращаемые значения
>>>>>>> master

Задает или возвращает значение **типа Variant** , которое указывает, сущности, представленной **записи**.

## <a name="remarks"></a>Замечания

Свойство **Source** возвращает *исходный* аргумент методу [Open](open-method-ado-record.md) объекта **записи** . Он может содержать абсолютное или относительное строку URL-адреса. Абсолютный URL-адрес может использоваться без установки свойства [ActiveConnection](activeconnection-property-ado.md) непосредственно открыть объект **записи** . В этом случае создается объект **подключения** неявных.

Свойство **Source** также может содержать ссылки на уже открытой **записей**, открывающий **записи** объект, представляющий текущую строку в **набора записей**.

Свойство **Source** может также содержать ссылку на объект [команды](command-object-ado.md) , который возвращает одну строку данных от поставщика.

Если задано свойство **ActiveConnection** , свойство **Source** должен указывать некоторые объект, который существует в пределах это подключение. Например в пространствах имен структура дерева, если свойство **Source** содержит абсолютный URL-адрес оно должно указывать на узел, который существует внутри области узла, определяемую средством URL-адрес в строку подключения. Если свойство **Source** содержит относительный URL-адрес, он проверяется в контексте, заданной свойством **ActiveConnection** .

Свойство **Source** — чтение и запись во время объект **записи** закрывается и доступен только для чтения, когда объект **записи** открыт.

<<<<<<< HEAD

> [!NOTE]
> <P>URL-адреса, с помощью схемы http автоматически вызывает <A href="microsoft-ole-db-provider-for-internet-publishing.md">Поставщик Microsoft OLE DB для публикации Интернет</A>. Для получения дополнительных сведений см <A href="absolute-and-relative-urls.md">абсолютного и относительных URL-адресов</A>.</P>
=======
> [!NOTE]
> URL-адреса, с помощью схемы http автоматически вызывает [Поставщик Microsoft OLE DB для публикации Интернет](microsoft-ole-db-provider-for-internet-publishing.md). Для получения дополнительных сведений см [абсолютных и относительных URL-адресов](absolute-and-relative-urls.md).
>>>>>>> master


