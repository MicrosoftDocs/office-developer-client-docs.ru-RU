---
title: SkipLine Method (ADO)
TOCTitle: SkipLine Method (ADO)
ms:assetid: 419c24c3-6b84-eed0-5884-f2dcd485dc3d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249187(v=office.15)
ms:contentKeyID: 48544456
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 28cb222a3ed0e5497e03efbb7394081c96b4d4ef
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25481493"
---
# <a name="skipline-method-ado"></a>SkipLine Method (ADO)


**Применимо к**: Access 2013 | Office 2013

Пропускает одну всю строку при чтении текстовый поток.

## <a name="syntax"></a>Синтаксис

*Поток*. SkipLine

## <a name="remarks"></a>Замечания

Все символы, включая Далее разделителя строки, пропускаются. По умолчанию [LineSeparator](lineseparator-property-ado.md) — **adCRLF**. При попытке пропустить [EOS](eos-property-ado.md)текущей позиции просто останется на **EOS**.

Метод **SkipLine** используется с потоками текст ([Тип](type-property-ado-stream.md) — **adTypeText**).

