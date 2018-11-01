---
title: Свойство Name (ADO MD)
TOCTitle: Name Property (ADO MD)
ms:assetid: 31ea6dad-c464-3af7-4b7a-086900656c2c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249093(v=office.15)
ms:contentKeyID: 48544065
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 63e098a8b97bb37fad2ef256affb2da142daf434
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25878649"
---
# <a name="name-property-ado-md"></a>Свойство Name (ADO MD)


**Применимо к**: Access 2013, Office 2013

Указывает имя объекта.

## <a name="return-values"></a>Возвращаемые значения

Возвращает **строку** и доступен только для чтения.

## <a name="remarks"></a>Замечания

Свойство **Name** объекта можно извлечь с помощью порядковый номер ссылки, после чего можно обратиться к объекту непосредственно по имени. Например если cdf. CubeDefs(0). Имя уступает «Bobs видео хранилища», можно ссылаться на этот [CubeDef](cubedef-object-ado-md.md) как cdf. CubeDefs ("Bobs видео хранилище").

