---
title: Свойство состояний (ADO MD)
TOCTitle: State Property (ADO MD)
ms:assetid: 4df09f45-9b62-33ce-b4ed-230e41eaac7a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249249(v=office.15)
ms:contentKeyID: 48544744
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4bc1efc33aa263275ba50526ff682b64a229293f
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25885467"
---
# <a name="state-property-ado-md"></a>Свойство состояний (ADO MD)


**Применимо к**: Access 2013, Office 2013

Указывает текущее состояние ячеек.

## <a name="return-values"></a>Возвращаемые значения

Возвращает **длинное** целое число, указывающее текущее состояние объекта [ячеек](cellset-object-ado-md.md) и доступен только для чтения. Допустимыми являются следующие значения: **adStateClosed** (0) и **adStateOpen** (1).

## <a name="remarks"></a>Замечания

Чтобы использовать имена констант [ObjectStateEnum](objectstateenum.md) , необходимо иметь на библиотеку типов ADO ссылается проект. [С помощью ADO с ADO MD](using-ado-with-ado-md.md) более подробные сведения.

