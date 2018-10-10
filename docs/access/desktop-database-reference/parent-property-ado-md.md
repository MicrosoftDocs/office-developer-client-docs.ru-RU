---
title: Parent Property (ADO MD)
TOCTitle: Parent Property (ADO MD)
ms:assetid: 62649da7-d35f-f11f-674c-28ce95abaf20
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249370(v=office.15)
ms:contentKeyID: 48545238
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: eb1606a745cb8572f54b253bdbbbbbb461cfc74a
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25481005"
---
# <a name="parent-property-ado-md"></a>Parent Property (ADO MD)


**Применимо к**: Access 2013 | Office 2013

Указывает элемент, являющийся родительским для текущего элемента в иерархии.

## <a name="return-values"></a>Return Values

Возвращает объект, [член](member-object-ado-md.md) и доступен только для чтения.

## <a name="remarks"></a>Замечания

Элемент, который находится на верхнем уровне иерархии (корень) не имеет родительского узла. Это свойство поддерживается только для объектов **члена** , относящегося к объекту [уровень](level-object-ado-md.md) . Ошибка происходит, когда это свойство является ссылка из объектов **члена** , относящегося к объекту [позиции](position-object-ado-md.md) .

