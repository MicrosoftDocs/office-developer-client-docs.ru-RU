---
title: Свойство DrilledDown (ADO MD)
TOCTitle: DrilledDown Property (ADO MD)
ms:assetid: 1dfe728f-8da2-1d2b-7361-8689a0b088b4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248972(v=office.15)
ms:contentKeyID: 48543610
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f7e53eb2a6d1735e07fa73e38adad8a59522fddf
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25871502"
---
# <a name="drilleddown-property-ado-md"></a>Свойство DrilledDown (ADO MD)


**Применимо к**: Access 2013, Office 2013

Указывает, будет ли дочерних элементов следовать непосредственно после элемента на оси.

## <a name="return-values"></a>Возвращаемые значения

Возвращает **логическое** значение и доступен только для чтения. **DrilledDown** возвращает **значение True** , если нет дочерних членов текущего элемента на оси. **DrilledDown** возвращает **значение False** , если один или несколько дочерних элементов текущего элемента на оси.

## <a name="remarks"></a>Замечания

Свойство **DrilledDown** используется для определения, существует ли хотя бы один дочерний этого элемента на оси сразу после этого элемента. Эта информация может быть полезна при отображении элемента.

Это свойство поддерживается только для объектов [члена](member-object-ado-md.md) , относящегося к объекту [позиции](position-object-ado-md.md) . Ошибка происходит, когда это свойство является ссылка из объектов **члена** , относящегося к объекту [уровень](level-object-ado-md.md) .

