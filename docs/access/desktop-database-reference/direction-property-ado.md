---
title: Direction Property (ADO)
TOCTitle: Direction Property (ADO)
ms:assetid: 51a94abb-7ce9-9adb-2b76-5391eb9f6863
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249262(v=office.15)
ms:contentKeyID: 48544823
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 611e5efbe53964c5ba255380e2659f024bd6be9a
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25481744"
---
# <a name="direction-property-ado"></a>Direction Property (ADO)


**Применимо к**: Access 2013 | Office 2013

Указывает [параметр](parameter-object-ado.md) представляет входного параметра, выходного параметра, входного и выходного параметра, или если параметр имеет значение, возвращаемое хранимой процедуры.

## <a name="settings-and-return-values"></a>Параметры и возвращаемые значения

Задает или возвращает значение [ParameterDirectionEnum](parameterdirectionenum.md) .

## <a name="remarks"></a>Замечания

Используйте свойство **направление** для указания передается как параметр или из процедуры. Является ли данное свойство **направление** чтения/записи; Это позволяет работать с поставщиками, которые не возвращают эти сведения или задать эти сведения при отсутствии ADO, чтобы сделать дополнительного обращения к поставщику для получения сведений о параметрах.

Не все поставщики можно определить направление параметры их хранимых процедур. В таких случаях необходимо задать свойство **направление** до выполнения запроса.

