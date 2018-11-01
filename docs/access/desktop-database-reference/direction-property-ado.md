---
title: Свойство Direction (ADO)
TOCTitle: Direction property (ADO)
ms:assetid: 51a94abb-7ce9-9adb-2b76-5391eb9f6863
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249262(v=office.15)
ms:contentKeyID: 48544823
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b9e34522a69b2e79f8ef44b912e2c0648c5b813d
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25881295"
---
# <a name="direction-property-ado"></a>Свойство Direction (ADO)


**Применимо к**: Access 2013, Office 2013

Указывает [параметр](parameter-object-ado.md) представляет входного параметра, выходного параметра, входного и выходного параметра, или если параметр имеет значение, возвращаемое хранимой процедуры.

## <a name="settings-and-return-values"></a>Параметры и возвращаемые значения

Задает или возвращает значение [ParameterDirectionEnum](parameterdirectionenum.md) .

## <a name="remarks"></a>Замечания

Используйте свойство **направление** для указания передается как параметр или из процедуры. Является ли данное свойство **направление** чтения/записи; Это позволяет работать с поставщиками, которые не возвращают эти сведения или задать эти сведения при отсутствии ADO, чтобы сделать дополнительного обращения к поставщику для получения сведений о параметрах.

Не все поставщики можно определить направление параметры их хранимых процедур. В таких случаях необходимо задать свойство **направление** до выполнения запроса.

