---
title: Свойство DrilledDown (ADO MD)
TOCTitle: DrilledDown property (ADO MD)
ms:assetid: 1dfe728f-8da2-1d2b-7361-8689a0b088b4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248972(v=office.15)
ms:contentKeyID: 48543610
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 40a97c7f755f681169c77c3a2077ee41d9cdc980
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293688"
---
# <a name="drilleddown-property-ado-md"></a>Свойство DrilledDown (ADO MD)


**Область применения**: Access 2013, Office 2013

Указывает, должны ли дочерние элементы сразу следовать за элементом на оси.

## <a name="return-values"></a>Возвращаемые значения

Возвращает **логическое** значение и доступно только для чтения. **DrilledDown** возвращает **значение true** , если на оси нет дочерних элементов текущего элемента. **DrilledDown** возвращает **значение false** , если один или несколько дочерних элементов текущего элемента оси.

## <a name="remarks"></a>Примечания

Используйте свойство **DrilledDown** , чтобы определить, есть ли по крайней мере один дочерний элемент этого элемента на оси, которая сразу после этого элемента. Эта информация полезна при отображении элемента.

Это свойство поддерживается только для объектов [member](member-object-ado-md.md) , принадлежащих объекту [position](position-object-ado-md.md) . При обращении к этому свойству из объектов **member** , принадлежащих объекту [уровня](level-object-ado-md.md) , возникает ошибка.

