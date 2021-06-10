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

Указывает источник данных или объект, представленный [записью.](record-object-ado.md)

## <a name="settings-and-return-values"></a>Параметры и значения возврата

Задает или возвращает значение **Variant,** которое указывает сущность, представленную **записью.**

## <a name="remarks"></a>Примечания

Свойство **Source** возвращает аргумент *Source* метода Открыть объект **Record.** [](open-method-ado-record.md) Она может содержать абсолютную или относительную строку URL-адреса. Абсолютный URL-адрес можно использовать без установки свойства [ActiveConnection](activeconnection-property-ado.md) для непосредственного открытия **объекта Запись.** В **этом** случае создается неявный объект Подключения.

Свойство **Source** также может содержать ссылку на уже открытый набор **recordset,** открывавший объект **Record,** представляющий текущую строку **в Наборе записей.**

Свойство **Source** также может содержать ссылку на объект [Command,](command-object-ado.md) который возвращает один ряд данных от поставщика.

Если также установлено свойство **ActiveConnection,** то свойство **Source** должно указать на объект, который существует в пределах этого подключения. Например, в пространствах имен с структурой дерева, если свойство **Source** содержит абсолютный URL-адрес, оно должно указать узел, который существует в области узла, идентифицированного URL-адресом в строке подключения. Если свойство **Source** содержит относительный URL-адрес, оно проверяется в контексте, задаемом **свойством ActiveConnection.**

Свойство **Source** читается или записуется во время закрытия объекта **Запись** и только для чтения, пока объект **Record** открыт.

> [!NOTE]
> URL-адреса, использующие схему http, автоматически вызывают поставщика DB Microsoft [OLE для публикации в Интернете.](microsoft-ole-db-provider-for-internet-publishing.md) Дополнительные сведения см. в [url-адресах Absolute и relative.](absolute-and-relative-urls.md)


