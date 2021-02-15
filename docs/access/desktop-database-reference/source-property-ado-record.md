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

## <a name="settings-and-return-values"></a>Параметры и возвращаемые значения

Задает или возвращает значение **Variant,** которое указывает сущность, представленную **записью.**

## <a name="remarks"></a>Заметки

Свойство **Source** возвращает аргумент *Source* метода Open объекта **Record.** [](open-method-ado-record.md) Он может содержать абсолютную или относительную строку URL-адреса. Абсолютный URL-адрес можно использовать без настройки свойства [ActiveConnection](activeconnection-property-ado.md) для непосредственного открытия **объекта Record.** В этом **случае** создается неявный объект Connection.

Свойство **Source** также может содержать ссылку на уже открытый набор записей, который открывает объект **Record,** представляющий текущую строку в **наборе записей.**

Свойство **Source** также может содержать ссылку на объект [Command,](command-object-ado.md) который возвращает одну строку данных от поставщика.

Если также установлено свойство **ActiveConnection,** свойство **Source** должно указать на какой-либо объект, который существует в области этого подключения. Например, в древоструктуренных пространствах имен, если свойство **Source** содержит абсолютный URL-адрес, оно должно указать узел, который существует в области узла, задаемого URL-адресом в строке подключения. Если свойство **Source** содержит относительный URL-адрес, оно проверяется в контексте, задаемом **свойством ActiveConnection.**

Свойство **Source** находится в режиме чтения и записи при закрытии объекта **Record,** а объект **Record** открыт только для чтения.

> [!NOTE]
> URL-адреса, использующие схему HTTP, автоматически вызывают поставщика [Microsoft OLE DB для интернет-публикации.](microsoft-ole-db-provider-for-internet-publishing.md) Дополнительные сведения см. в [сведениях об абсолютных и относительных URL-адресах.](absolute-and-relative-urls.md)


