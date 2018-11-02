---
title: Свойство State (ADO MD)
TOCTitle: State property (ADO MD)
ms:assetid: 4df09f45-9b62-33ce-b4ed-230e41eaac7a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249249(v=office.15)
ms:contentKeyID: 48544744
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 33933fb71ee3d7541640469eebc650c0f52a9784
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25922015"
---
# <a name="state-property-ado-md"></a>Свойство State (ADO MD)


**Применимо к**: Access 2013, Office 2013

Указывает текущее состояние ячеек.

## <a name="return-values"></a>Возвращаемые значения

Возвращает **длинное** целое число, указывающее текущее состояние объекта [ячеек](cellset-object-ado-md.md) и доступен только для чтения. Допустимыми являются следующие значения: **adStateClosed** (0) и **adStateOpen** (1).

## <a name="remarks"></a>Примечания

Чтобы использовать имена констант [ObjectStateEnum](objectstateenum.md) , необходимо иметь на библиотеку типов ADO ссылается проект. [С помощью ADO с ADO MD](using-ado-with-ado-md.md) более подробные сведения.

