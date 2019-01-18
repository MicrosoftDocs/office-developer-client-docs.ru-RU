---
title: Свойство EOS (ADO - ссылки для настольных баз данных Access))
TOCTitle: EOS property (ADO)
ms:assetid: 97cd23ef-cca8-4dcc-2641-082a0e1b853c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249676(v=office.15)
ms:contentKeyID: 48546474
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a35503fb0ad320e82ed385c7014b2a18de586064
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28716602"
---
# <a name="eos-property-ado"></a>Свойство EOS (ADO)


**Применимо к**: Access 2013, Office 2013

Указывает, является ли текущую позицию в конце потока.

## <a name="return-values"></a>Возвращаемые значения

Возвращает **логическое** значение, указывающее, является ли текущую позицию в конце потока. **EOS** возвращает **значение True,** Если нет больше байтов в поток; Если существует несколько байт после текущего положения возвращает **значение False** .

Чтобы задать конец потока позицию, используйте метод [SetEOS](seteos-method-ado.md) . Чтобы определить текущую позицию, используйте свойство [положение](position-property-ado.md) .

