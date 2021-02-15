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

Указывает, не следует ли сразу следовать за членом на оси.

## <a name="return-values"></a>Возвращаемые значения

Возвращает значение **boolean** и является только для чтения. **DrilledDown** возвращает **true,** если на оси нет других членов текущего члена. **DrilledDown** возвращает **false,** если на оси имеется один или несколько членов текущего члена.

## <a name="remarks"></a>Заметки

Используйте свойство **DrilledDown,** чтобы определить, есть ли по крайней мере один child этого члена на оси сразу после этого члена. Эти сведения полезны при отобрале участника.

Это свойство поддерживается только для объектов [Member,](member-object-ado-md.md) принадлежащих [объекту Position.](position-object-ado-md.md) Ошибка возникает, когда на это свойство ссылается объект **Member,** принадлежащий [объекту Level.](level-object-ado-md.md)

