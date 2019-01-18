---
title: Свойство Parent (ADO MD)
TOCTitle: Parent property (ADO MD)
ms:assetid: 62649da7-d35f-f11f-674c-28ce95abaf20
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249370(v=office.15)
ms:contentKeyID: 48545238
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e0c0eef638cb76676cd2287a34c0e4b17bd89c4d
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28700003"
---
# <a name="parent-property-ado-md"></a>Свойство Parent (ADO MD)


**Применимо к**: Access 2013, Office 2013

Указывает элемент, являющийся родительским для текущего элемента в иерархии.

## <a name="return-values"></a>Возвращаемые значения

Возвращает объект, [член](member-object-ado-md.md) и доступен только для чтения.

## <a name="remarks"></a>Замечания

Элемент, который находится на верхнем уровне иерархии (корень) не имеет родительского узла. Это свойство поддерживается только для объектов **члена** , относящегося к объекту [уровень](level-object-ado-md.md) . Ошибка происходит, когда это свойство является ссылка из объектов **члена** , относящегося к объекту [позиции](position-object-ado-md.md) .

