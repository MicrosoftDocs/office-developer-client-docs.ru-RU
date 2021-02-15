---
title: Метод SetEOS (ADO)
TOCTitle: SetEOS method (ADO)
ms:assetid: d438eecf-7ab3-a07d-b6d5-8816db4aae7c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250063(v=office.15)
ms:contentKeyID: 48547933
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 5f3b1ee81928a8da77cc3edff7f1feffb7196bba
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308710"
---
# <a name="seteos-method-ado"></a>Метод SetEOS (ADO)

**Область применения**: Access 2013, Office 2013

Задает положение, которое является окончанием потока.

## <a name="syntax"></a>Синтаксис

*Stream*. SetEOS

## <a name="remarks"></a>Заметки

**SetEOS** обновляет значение свойства [EOS,](eos-property-ado.md) делая [](position-property-ado.md) текущую позицию конечной частью потока. Все bytes или characters following the current position are truncated.

Так как [write,](write-method-ado.md) [WriteText](writetext-method-ado.md)и [CopyTo](copyto-method-ado.md) не укорачивать дополнительные значения в существующих объектах **Stream,** вы можете усечь эти значения или символы, задав новую позицию конечного потока с **помощью SetEOS.**

> [!WARNING]
> Если вы установите **для EOS** положение перед фактическим завершением потока, вы потеряете все данные после новой позиции **EOS.**
