---
title: Свойство state (ADO MD)
TOCTitle: State property (ADO MD)
ms:assetid: 4df09f45-9b62-33ce-b4ed-230e41eaac7a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249249(v=office.15)
ms:contentKeyID: 48544744
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 051a9f0cc50ae3a60edb033f6807f72fc0688976
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306365"
---
# <a name="state-property-ado-md"></a>Свойство state (ADO MD)


**Область применения**: Access 2013, Office 2013

Указывает текущее состояние ячейки.

## <a name="return-values"></a>Возвращаемые значения

Возвращает **длинное** количество, указывающее текущее состояние объекта [Cellset,](cellset-object-ado-md.md) и только для чтения. Допустимы следующие значения: **adStateClosed** (0) и **adStateOpen** (1).

## <a name="remarks"></a>Примечания

Чтобы использовать [постоянные имена ObjectStateEnum,](objectstateenum.md) в проекте должна быть ссылаться библиотека типов ADO. Дополнительные сведения см. [в использовании ADO с ADO MD.](using-ado-with-ado-md.md)

