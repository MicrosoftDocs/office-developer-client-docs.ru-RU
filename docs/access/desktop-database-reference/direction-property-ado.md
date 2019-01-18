---
title: Свойство Direction (ADO)
TOCTitle: Direction property (ADO)
ms:assetid: 51a94abb-7ce9-9adb-2b76-5391eb9f6863
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249262(v=office.15)
ms:contentKeyID: 48544823
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 5885e89a3bce5d8b16ea855ce14689380655ad45
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28706333"
---
# <a name="direction-property-ado"></a>Свойство Direction (ADO)


**Применимо к**: Access 2013, Office 2013

Указывает [параметр](parameter-object-ado.md) представляет входного параметра, выходного параметра, входного и выходного параметра, или если параметр имеет значение, возвращаемое хранимой процедуры.

## <a name="settings-and-return-values"></a>Параметры и возвращаемые значения

Задает или возвращает значение [ParameterDirectionEnum](parameterdirectionenum.md) .

## <a name="remarks"></a>Замечания

Используйте свойство **направление** для указания передается как параметр или из процедуры. Является ли данное свойство **направление** чтения/записи; Это позволяет работать с поставщиками, которые не возвращают эти сведения или задать эти сведения при отсутствии ADO, чтобы сделать дополнительного обращения к поставщику для получения сведений о параметрах.

Не все поставщики можно определить направление параметры их хранимых процедур. В таких случаях необходимо задать свойство **направление** до выполнения запроса.

