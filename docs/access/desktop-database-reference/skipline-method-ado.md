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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28718779"
---
# <a name="skipline-method-ado"></a>Метод SkipLine (ADO)


**Применимо к**: Access 2013, Office 2013

Пропускает одну всю строку при чтении текстовый поток.

## <a name="syntax"></a>Синтаксис

*Поток*. SkipLine

## <a name="remarks"></a>Замечания

Все символы, включая Далее разделителя строки, пропускаются. По умолчанию [LineSeparator](lineseparator-property-ado.md) — **adCRLF**. При попытке пропустить [EOS](eos-property-ado.md)текущей позиции просто останется на **EOS**.

Метод **SkipLine** используется с потоками текст ([Тип](type-property-ado-stream.md) — **adTypeText**).

