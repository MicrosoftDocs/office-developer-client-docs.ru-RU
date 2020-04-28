---
title: Свойство Ordinal (Cell в ADO MD)
TOCTitle: Ordinal property (ADO MD Cell)
ms:assetid: be705823-6c5e-0c8f-f780-87df19423a72
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249924(v=office.15)
ms:contentKeyID: 48547462
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 91b8d66929e360f88385b6773a03fcaffb79161d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288205"
---
# <a name="ordinal-property-ado-md-cell"></a>Свойство Ordinal (Cell в ADO MD)


**Область применения**: Access 2013, Office 2013

Уникально определяет ячейку по ее позиции в наборе ячеек.

## <a name="return-values"></a>Возвращаемые значения

Возвращает целое значение **типа Long** и доступно только для чтения.

## <a name="remarks"></a>Примечания

Порядковое значение ячейки однозначно определяет ячейку в наборе ячеек. Как концептуально, ячейки пронумерованы *в наборе*ячеек, как если бы набор ячеек был одномерным массивом, где *p* — это количество [осей](axes-collection-ado-md.md). Нумерация ячеек начинается с нуля в порядке строки основной.

Порядковое значение ячейки можно использовать вместе со свойством [Item](item-property-ado-md-cellset.md) объекта [Cell](cellset-object-ado-md.md) , чтобы быстро извлечь [ячейку](cell-object-ado-md.md).

