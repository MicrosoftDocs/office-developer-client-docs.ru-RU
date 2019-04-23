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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288660"
---
# <a name="name-property-ado-md"></a>Свойство Name (ADO MD)


**Область применения**: Access 2013, Office 2013

Указывает имя объекта.

## <a name="return-values"></a>Возвращаемые значения

Возвращает **строку** и доступна только для чтения.

## <a name="remarks"></a>Замечания

Вы можете получить свойство **Name** объекта по порядковому номеру, после чего вы можете ссылаться на объект напрямую по имени. Например, если CDF. Коллекция cubedefs (0). Name дает "Бобс Video Store", вы можете ссылаться на этот [CubeDef](cubedef-object-ado-md.md) как на CDF. Коллекция cubedefs ("Бобс Video Store").

