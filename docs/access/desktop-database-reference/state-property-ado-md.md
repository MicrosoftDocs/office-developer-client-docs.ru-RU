---
title: State Property (ADO MD)
TOCTitle: State Property (ADO MD)
ms:assetid: 4df09f45-9b62-33ce-b4ed-230e41eaac7a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249249(v=office.15)
ms:contentKeyID: 48544744
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a42ade39a50eb5dc40e213d6f4c3f4ed0ba3475e
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25481245"
---
# <a name="state-property-ado-md"></a>State Property (ADO MD)


**Применимо к**: Access 2013 | Office 2013

Указывает текущее состояние ячеек.

## <a name="return-values"></a>Return Values

Возвращает **длинное** целое число, указывающее текущее состояние объекта [ячеек](cellset-object-ado-md.md) и доступен только для чтения. Допустимыми являются следующие значения: **adStateClosed** (0) и **adStateOpen** (1).

## <a name="remarks"></a>Замечания

Чтобы использовать имена констант [ObjectStateEnum](objectstateenum.md) , необходимо иметь на библиотеку типов ADO ссылается проект. [С помощью ADO с ADO MD](using-ado-with-ado-md.md) более подробные сведения.

