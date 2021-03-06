---
title: Метод Close (ADO MD)
TOCTitle: Close method (ADO MD)
ms:assetid: 683788b0-0a96-a165-6b49-8d7036850756
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249406(v=office.15)
ms:contentKeyID: 48545382
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 609069d04124146f311166e3ae56d8d6a793675b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296320"
---
# <a name="close-method-ado-md"></a>Метод Close (ADO MD)


**Область применения**: Access 2013, Office 2013

Закрывает открытый ячейки.

## <a name="syntax"></a>Синтаксис

*Cellset*. Закрыть

## <a name="remarks"></a>Примечания

С помощью **метода Close** для закрытия объекта [Cellset](cellset-object-ado-md.md) будут высвобованы связанные данные, в том числе данные в любых связанных объектах [Cell,](cell-object-ado-md.md) [Axis,](axis-object-ado-md.md) [Position](position-object-ado-md.md)или [Member.](member-object-ado-md.md) Закрытие **ячейки не** удаляет его из памяти; Вы можете изменить его параметры свойств и открыть его позже. Чтобы полностью исключить объект из памяти, установите переменную объекта **в Nothing**.

Позже можно вызвать метод [Open,](open-method-ado-md.md) чтобы открыть **ячейки** с помощью той же или другой строки источника. В то время как объект **Cellset** закрыт, при сборе любых свойств или вызове любых методов, ссылающихся на данные или метаданные, создает ошибку.

