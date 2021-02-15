---
title: EOS Property (ADO - Access desktop database reference))
TOCTitle: EOS property (ADO)
ms:assetid: 97cd23ef-cca8-4dcc-2641-082a0e1b853c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249676(v=office.15)
ms:contentKeyID: 48546474
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a35503fb0ad320e82ed385c7014b2a18de586064
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293527"
---
# <a name="eos-property-ado"></a>Свойство EOS (ADO)


**Область применения**: Access 2013, Office 2013

Указывает, находится ли текущая позиция в конце потока.

## <a name="return-values"></a>Возвращаемые значения

Возвращает **boolean значение,** которое указывает, находится ли текущая позиция в конце потока. **EOS** возвращает **true,** если в потоке больше нет данных; Если **текущее** положение больше, возвращается false.

Чтобы установить конец положения потока, используйте метод [SetEOS.](seteos-method-ado.md) Чтобы определить текущую позицию, используйте [свойство Position.](position-property-ado.md)

