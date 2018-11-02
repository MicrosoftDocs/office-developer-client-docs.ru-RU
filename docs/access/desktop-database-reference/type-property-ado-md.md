---
title: Свойство Type (ADO MD)
TOCTitle: Type property (ADO MD)
ms:assetid: 4aaa151e-1f02-aa7d-a9e5-e7019b200924
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249230(v=office.15)
ms:contentKeyID: 48544671
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3f5cffb5fb888298b23dad02d9593978e581aa6c
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25928749"
---
# <a name="type-property-ado-md"></a>Свойство Type (ADO MD)


**Применимо к**: Access 2013, Office 2013

Указывает тип текущего элемента.

## <a name="return-values"></a>Возвращаемые значения

Возвращает значение [MemberTypeEnum](membertypeenum.md) и доступен только для чтения.

## <a name="remarks"></a>Примечания

Это свойство поддерживается только для объектов [члена](member-object-ado-md.md) , относящегося к объекту [уровень](level-object-ado-md.md) . Ошибка происходит, когда это свойство является ссылка из объектов **члена** , относящегося к объекту [позиции](position-object-ado-md.md) .

