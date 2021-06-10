---
title: Объект Каталог (ADO MD)
TOCTitle: Catalog object (ADO MD)
ms:assetid: 708c4082-3589-7f3b-5ea3-f3705f3d3ff1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249445(v=office.15)
ms:contentKeyID: 48545559
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0ee7d2e68df90c8eee4227f949f93ea074b7df97
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296593"
---
# <a name="catalog-object-ado-md"></a>Объект Каталог (ADO MD)


**Область применения**: Access 2013, Office 2013

Содержит многомерные сведения о схеме (т. е. кубов и их ниже, иерархий, уровней и членов), специфичные для многомерного поставщика данных (MDP).

## <a name="remarks"></a>Примечания

С коллекциями и свойствами объекта **Каталог** можно сделать следующее:

- Откройте каталог, установив свойство [ActiveConnection](activeconnection-property-ado-md.md) на стандартный объект ADO [Connection](connection-object-ado.md) или допустимую строку подключения.

- Определите **каталог** с [свойством Name.](name-property-ado-md.md)

- Итерировать кубов в каталоге с помощью [коллекции CubeDefs.](cubedefs-collection-ado-md.md)

