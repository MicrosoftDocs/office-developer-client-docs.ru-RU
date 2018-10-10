---
title: Свойство EOS (ADO - ссылки для настольных баз данных Access))
TOCTitle: EOS Property (ADO)
ms:assetid: 97cd23ef-cca8-4dcc-2641-082a0e1b853c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249676(v=office.15)
ms:contentKeyID: 48546474
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d4c6d96e2c143cb0548a2de987f11ea708d1669a
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25481382"
---
# <a name="eos-property-ado"></a>EOS Property (ADO)


**Применимо к**: Access 2013 | Office 2013

Указывает, является ли текущую позицию в конце потока.

## <a name="return-values"></a>Return Values

Возвращает **логическое** значение, указывающее, является ли текущую позицию в конце потока. **EOS** возвращает **значение True,** Если нет больше байтов в поток; Если существует несколько байт после текущего положения возвращает **значение False** .

Чтобы задать конец потока позицию, используйте метод [SetEOS](seteos-method-ado.md) . Чтобы определить текущую позицию, используйте свойство [положение](position-property-ado.md) .

