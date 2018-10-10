---
title: Type Property (ADO MD)
TOCTitle: Type Property (ADO MD)
ms:assetid: 4aaa151e-1f02-aa7d-a9e5-e7019b200924
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249230(v=office.15)
ms:contentKeyID: 48544671
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f3ea67b96e24f01e167ca693dff356c595005904
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25479783"
---
# <a name="type-property-ado-md"></a>Type Property (ADO MD)


**Применимо к**: Access 2013 | Office 2013

Указывает тип текущего элемента.

## <a name="return-values"></a>Return Values

Возвращает значение [MemberTypeEnum](membertypeenum.md) и доступен только для чтения.

## <a name="remarks"></a>Замечания

Это свойство поддерживается только для объектов [члена](member-object-ado-md.md) , относящегося к объекту [уровень](level-object-ado-md.md) . Ошибка происходит, когда это свойство является ссылка из объектов **члена** , относящегося к объекту [позиции](position-object-ado-md.md) .

