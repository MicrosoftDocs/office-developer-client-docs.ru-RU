---
title: Объект Catalog (ADO MD)
TOCTitle: Catalog object (ADO MD)
ms:assetid: 708c4082-3589-7f3b-5ea3-f3705f3d3ff1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249445(v=office.15)
ms:contentKeyID: 48545559
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1dd402a27164b5fb40bab10d7809f042846e37b5
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/03/2018
ms.locfileid: "25943733"
---
# <a name="catalog-object-ado-md"></a>Объект Catalog (ADO MD)


**Применимо к**: Access 2013, Office 2013

Содержит многомерные сведения о схеме (то есть, кубов и базовым измерений, иерархии, уровни и элементы) определенного поставщика многомерных данных (MDP).

## <a name="remarks"></a>Примечания

Со свойствами объекта **каталога** и семейств сайтов выполните следующее:

- Откройте каталог путем установки свойства [ActiveConnection](activeconnection-property-ado-md.md) стандартный объект ADO- [подключение](connection-object-ado.md) или это допустимая строка подключения.

- Определение **каталога** с помощью свойства [Name](name-property-ado-md.md) .

- Выполните итерацию по кубов в каталог с помощью коллекции [CubeDefs](cubedefs-collection-ado-md.md) .

