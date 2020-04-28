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

Задает позицию, которая является концом потока.

## <a name="syntax"></a>Синтаксис

*Stream*. SetEOS

## <a name="remarks"></a>Примечания

**SetEOS** обновляет значение свойства [EOS](eos-property-ado.md) , выполнив текущую [позицию](position-property-ado.md) в конце потока. Все байты и символы, следующие за текущей позицией, усекаются.

Так как [Write](write-method-ado.md), [WriteText](writetext-method-ado.md)и [CopyTo](copyto-method-ado.md) не усекаются никакие лишние значения в существующих объектах **потока** , можно усечь эти байты или символы, установив новую позицию конца потока в **SetEOS**.

> [!WARNING]
> Если для **EOS** задано положение до фактического конца потока, все данные после новой позиции **EOS** будут потеряны.
