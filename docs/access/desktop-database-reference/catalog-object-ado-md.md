---
title: Объект Catalog (ADO MD)
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
# <a name="catalog-object-ado-md"></a>Объект Catalog (ADO MD)


**Область применения**: Access 2013, Office 2013

Содержит сведения о многомерной схеме (то есть Кубы и базовые измерения, иерархии, уровни и элементы), характерные для поставщика многомерных данных (МДП).

## <a name="remarks"></a>Примечания

С помощью коллекций и свойств объекта **Catalog** можно выполнить следующие действия:

- Откройте каталог, задав для свойства [ActiveConnection](activeconnection-property-ado-md.md) стандартный объект [подключения](connection-object-ado.md) ADO или допустимую строку подключения.

- Определите **Каталог** со свойством [Name](name-property-ado-md.md) .

- Выполните итерацию по кубам в каталоге, используя коллекцию [коллекция cubedefs](cubedefs-collection-ado-md.md) .

