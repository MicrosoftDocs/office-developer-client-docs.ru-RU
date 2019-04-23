---
title: Метод SkipLine (ADO)
TOCTitle: SkipLine method (ADO)
ms:assetid: 419c24c3-6b84-eed0-5884-f2dcd485dc3d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249187(v=office.15)
ms:contentKeyID: 48544456
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 5e49b8379f078ad698a4a0040de0eb2e4429fd34
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314562"
---
# <a name="skipline-method-ado"></a>Метод SkipLine (ADO)


**Область применения**: Access 2013, Office 2013

ПроПускает одну строку целиком при чтении текстового потока.

## <a name="syntax"></a>Синтаксис

*Stream*. SkipLine

## <a name="remarks"></a>Примечания

Все символы до и включительно разделитель в следующую строку будут пропущены. По умолчанию [LineSeparator](lineseparator-property-ado.md) — **адкрлф**. Если вы попытаетесь пропустить прошедший [EOS](eos-property-ado.md), текущее положение просто останется в **EOS**.

Метод **SkipLine** используется с текстовыми потоками ([Type](type-property-ado-stream.md) — **адтипетекст**).

