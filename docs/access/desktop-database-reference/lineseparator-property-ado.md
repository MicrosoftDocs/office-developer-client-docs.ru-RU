---
title: Свойство LineSeparator (ADO)
TOCTitle: LineSeparator property (ADO)
ms:assetid: 9f1323cd-d4ed-2bfa-554b-faebab529548
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249729(v=office.15)
ms:contentKeyID: 48546676
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 831b6377ade43b3be04ed21add20fbd10e48ac2f
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25882506"
---
# <a name="lineseparator-property-ado"></a>Свойство LineSeparator (ADO)


**Применимо к**: Access 2013, Office 2013

Указывает двоичных символов для использования в качестве разделителя строки в объектах [потока](stream-object-ado.md) текста.

## <a name="settings-and-return-values"></a>Параметры и возвращаемые значения

Задает или возвращает [LineSeparatorsEnum](lineseparatorsenum.md) значение, указывающее знак разделителя строки, используемые в **поток**. Значение по умолчанию — **adCRLF**.

## <a name="remarks"></a>Замечания

**LineSeparator** используется для интерпретации строки при чтении содержимое текста **потока**. С помощью метода [SkipLine](skipline-method-ado.md) можно пропустить строки.

**LineSeparator** используется только с объектами **потока** текста ([Тип](type-property-ado-stream.md) — **adTypeText**). Это свойство игнорируется, если **Тип** — **adTypeBinary**.

