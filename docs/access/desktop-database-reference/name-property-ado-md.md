---
title: Свойство Name (ADO MD)
TOCTitle: Name property (ADO MD)
ms:assetid: 31ea6dad-c464-3af7-4b7a-086900656c2c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249093(v=office.15)
ms:contentKeyID: 48544065
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e4e27870a0c1dbb38b7c0be31c439a95f6aae671
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28704156"
---
# <a name="name-property-ado-md"></a>Свойство Name (ADO MD)


**Применимо к**: Access 2013, Office 2013

Указывает имя объекта.

## <a name="return-values"></a>Возвращаемые значения

Возвращает **строку** и доступен только для чтения.

## <a name="remarks"></a>Замечания

Свойство **Name** объекта можно извлечь с помощью порядковый номер ссылки, после чего можно обратиться к объекту непосредственно по имени. Например если cdf. CubeDefs(0). Имя уступает «Bobs видео хранилища», можно ссылаться на этот [CubeDef](cubedef-object-ado-md.md) как cdf. CubeDefs ("Bobs видео хранилище").

