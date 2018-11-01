---
title: Объект каталога (ADO MD)
TOCTitle: Catalog Object (ADO MD)
ms:assetid: 708c4082-3589-7f3b-5ea3-f3705f3d3ff1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249445(v=office.15)
ms:contentKeyID: 48545559
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: be9d55969a0f90595f25deac0b01a70bff6fc7c3
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25879601"
---
# <a name="catalog-object-ado-md"></a>Объект каталога (ADO MD)


**Применимо к**: Access 2013, Office 2013

Содержит многомерные сведения о схеме (то есть, кубов и базовым измерений, иерархии, уровни и элементы) определенного поставщика многомерных данных (MDP).

## <a name="remarks"></a>Замечания

Со свойствами объекта **каталога** и семейств сайтов выполните следующее:

  - Откройте каталог путем установки свойства [ActiveConnection](activeconnection-property-ado-md.md) стандартный объект ADO- [подключение](connection-object-ado.md) или это допустимая строка подключения.

  - Определение **каталога** с помощью свойства [Name](name-property-ado-md.md) .

  - Выполните итерацию по кубов в каталог с помощью коллекции [CubeDefs](cubedefs-collection-ado-md.md) .

