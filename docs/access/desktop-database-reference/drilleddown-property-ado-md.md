---
title: DrilledDown Property (ADO MD)
TOCTitle: DrilledDown Property (ADO MD)
ms:assetid: 1dfe728f-8da2-1d2b-7361-8689a0b088b4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248972(v=office.15)
ms:contentKeyID: 48543610
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 96edfa035937a201891f0dca2aeaf036a5061cfe
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/17/2018
ms.locfileid: "25605494"
---
# <a name="drilleddown-property-ado-md"></a>DrilledDown Property (ADO MD)


**Применимо к**: Access 2013 | Office 2013

Указывает, будет ли дочерних элементов следовать непосредственно после элемента на оси.

<<<<<<< HEAD
## <a name="return-values"></a>Return Values
=======
## <a name="return-values"></a>Возвращаемые значения
>>>>>>> master

Возвращает **логическое** значение и доступен только для чтения. **DrilledDown** возвращает **значение True** , если нет дочерних членов текущего элемента на оси. **DrilledDown** возвращает **значение False** , если один или несколько дочерних элементов текущего элемента на оси.

## <a name="remarks"></a>Замечания

Свойство **DrilledDown** используется для определения, существует ли хотя бы один дочерний этого элемента на оси сразу после этого элемента. Эта информация может быть полезна при отображении элемента.

Это свойство поддерживается только для объектов [члена](member-object-ado-md.md) , относящегося к объекту [позиции](position-object-ado-md.md) . Ошибка происходит, когда это свойство является ссылка из объектов **члена** , относящегося к объекту [уровень](level-object-ado-md.md) .

