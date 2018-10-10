---
title: Name Property (ADO MD)
TOCTitle: Name Property (ADO MD)
ms:assetid: 31ea6dad-c464-3af7-4b7a-086900656c2c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249093(v=office.15)
ms:contentKeyID: 48544065
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0cc7a89e0d6b9cdaed2c54d3269b61280ce3306c
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25480560"
---
# <a name="name-property-ado-md"></a>Name Property (ADO MD)


**Применимо к**: Access 2013 | Office 2013

Указывает имя объекта.

## <a name="return-values"></a>Return Values

Возвращает **строку** и доступен только для чтения.

## <a name="remarks"></a>Замечания

Свойство **Name** объекта можно извлечь с помощью порядковый номер ссылки, после чего можно обратиться к объекту непосредственно по имени. Например если cdf. CubeDefs(0). Имя уступает «Bobs видео хранилища», можно ссылаться на этот [CubeDef](cubedef-object-ado-md.md) как cdf. CubeDefs ("Bobs видео хранилище").

