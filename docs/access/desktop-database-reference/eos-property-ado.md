---
title: Свойство EOS (ADO - ссылки для настольных баз данных Access))
TOCTitle: EOS property (ADO)
ms:assetid: 97cd23ef-cca8-4dcc-2641-082a0e1b853c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249676(v=office.15)
ms:contentKeyID: 48546474
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 32b76259f9be90ebd60cbc8c618a4d2bb80de165
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25870123"
---
# <a name="eos-property-ado"></a>Свойство EOS (ADO)


**Применимо к**: Access 2013, Office 2013

Указывает, является ли текущую позицию в конце потока.

## <a name="return-values"></a>Возвращаемые значения

Возвращает **логическое** значение, указывающее, является ли текущую позицию в конце потока. **EOS** возвращает **значение True,** Если нет больше байтов в поток; Если существует несколько байт после текущего положения возвращает **значение False** .

Чтобы задать конец потока позицию, используйте метод [SetEOS](seteos-method-ado.md) . Чтобы определить текущую позицию, используйте свойство [положение](position-property-ado.md) .

