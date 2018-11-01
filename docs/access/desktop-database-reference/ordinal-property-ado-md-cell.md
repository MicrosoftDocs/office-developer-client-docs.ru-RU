---
title: Свойство порядковый номер (ADO MD ячейки)
TOCTitle: Ordinal Property (ADO MD Cell)
ms:assetid: be705823-6c5e-0c8f-f780-87df19423a72
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249924(v=office.15)
ms:contentKeyID: 48547462
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: fa85626b0de3a907d5a7ebf79cf333f76f42426e
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25867981"
---
# <a name="ordinal-property-ado-md-cell"></a>Свойство порядковый номер (ADO MD ячейки)


**Применимо к**: Access 2013, Office 2013

Однозначно определяет ячейку по ее позиции в рамках набора ячеек.

## <a name="return-values"></a>Возвращаемые значения

Возвращает значение типа **Long** integer и доступен только для чтения.

## <a name="remarks"></a>Замечания

Порядковый номер ячейки однозначно определяет ячейку в рамках набора ячеек. Концептуально ячеек нумеруются в набора ячеек, как будто ячеек *p*-двумерного массива array, где *p* — это число [осей](axes-collection-ado-md.md). Ячейки нумеруются, начиная с нуля в строкам.

Порядковый номер ячейки можно использовать свойство [Item](item-property-ado-md-cellset.md) объекта [ячеек](cellset-object-ado-md.md) для быстрого извлечения [ячейки](cell-object-ado-md.md).

