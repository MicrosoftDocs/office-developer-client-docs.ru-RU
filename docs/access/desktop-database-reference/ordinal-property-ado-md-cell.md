---
title: Ordinal Property (ADO MD Cell)
TOCTitle: Ordinal Property (ADO MD Cell)
ms:assetid: be705823-6c5e-0c8f-f780-87df19423a72
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249924(v=office.15)
ms:contentKeyID: 48547462
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0e067fbc90a0e05d31611d7284a735cf1cfe6aa1
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/17/2018
ms.locfileid: "25606782"
---
# <a name="ordinal-property-ado-md-cell"></a>Ordinal Property (ADO MD Cell)


**Применимо к**: Access 2013 | Office 2013

Однозначно определяет ячейку по ее позиции в рамках набора ячеек.

<<<<<<< HEAD
## <a name="return-values"></a>Return Values
=======
## <a name="return-values"></a>Возвращаемые значения
>>>>>>> master

Возвращает значение типа **Long** integer и доступен только для чтения.

## <a name="remarks"></a>Замечания

Порядковый номер ячейки однозначно определяет ячейку в рамках набора ячеек. Концептуально ячеек нумеруются в набора ячеек, как будто ячеек *p*-двумерного массива array, где *p* — это число [осей](axes-collection-ado-md.md). Ячейки нумеруются, начиная с нуля в строкам.

Порядковый номер ячейки можно использовать свойство [Item](item-property-ado-md-cellset.md) объекта [ячеек](cellset-object-ado-md.md) для быстрого извлечения [ячейки](cell-object-ado-md.md).

