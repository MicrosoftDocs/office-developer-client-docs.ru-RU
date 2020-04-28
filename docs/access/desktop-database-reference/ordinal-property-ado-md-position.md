---
title: Свойство Ordinal (Position в ADO MD)
TOCTitle: Ordinal property (ADO MD Position)
ms:assetid: fb132ab5-d2b5-317d-e885-5e37ddaf90fb
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250284(v=office.15)
ms:contentKeyID: 48548861
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2e29b5c86e8f37d84116aa92432e93eb8943e29e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288192"
---
# <a name="ordinal-property-ado-md-position"></a>Свойство Ordinal (Position в ADO MD)


**Область применения**: Access 2013, Office 2013

Уникально определяет положение вдоль оси.

## <a name="return-values"></a>Возвращаемые значения

Возвращает целое значение **типа Long** и доступно только для чтения.

## <a name="remarks"></a>Примечания

**Порядковый номер** объекта [position](position-object-ado-md.md) соответствует индексу **позиции** в коллекции [Positions](positions-collection-ado-md.md) .

Ячейка может быстро извлекаться с помощью **порядкового номера** **позиции** на каждой оси со свойством [Item](item-property-ado-md-cellset.md) объекта набора [ячеек](cellset-object-ado-md.md) .

