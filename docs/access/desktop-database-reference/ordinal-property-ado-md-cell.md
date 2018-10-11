---
title: Ordinal Property (ADO MD Cell)
TOCTitle: Ordinal Property (ADO MD Cell)
ms:assetid: be705823-6c5e-0c8f-f780-87df19423a72
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249924(v=office.15)
ms:contentKeyID: 48547462
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 284e2cac2c1a86d87e39d9913a262fbafb435ece
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25480519"
---
# <a name="ordinal-property-ado-md-cell"></a>Ordinal Property (ADO MD Cell)


**Применимо к**: Access 2013 | Office 2013

Однозначно определяет ячейку по ее позиции в рамках набора ячеек.

## <a name="return-values"></a>Return Values

Возвращает значение типа **Long** integer и доступен только для чтения.

## <a name="remarks"></a>Замечания

Порядковый номер ячейки однозначно определяет ячейку в рамках набора ячеек. Концептуально ячеек нумеруются в набора ячеек, как будто ячеек *p*-двумерного массива array, где *p* — это число [осей](axes-collection-ado-md.md). Ячейки нумеруются, начиная с нуля в строкам.

Порядковый номер ячейки можно использовать свойство [Item](item-property-ado-md-cellset.md) объекта [ячеек](cellset-object-ado-md.md) для быстрого извлечения [ячейки](cell-object-ado-md.md).

