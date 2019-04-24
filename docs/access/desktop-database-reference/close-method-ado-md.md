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

ЗаКрывает открытый набор ячеек.

## <a name="syntax"></a>Синтаксис

Набор *ячеек*. Закрыть

## <a name="remarks"></a>Замечания

С помощью метода **Close** для закрытия объекта набор [ячеек](cellset-object-ado-md.md) будут освобождены связанные данные, включая данные в любой связанной [ячейке](cell-object-ado-md.md), [оси](axis-object-ado-md.md), [позиции](position-object-ado-md.md)или объекте [элемента](member-object-ado-md.md) . При закрытии набор **ячеек** не удаляется из памяти; Вы можете изменить его свойства и открыть позже. Чтобы полностью удалить объект из памяти, присвойте переменной объекта значение **Nothing**.

Позже можно вызвать метод [Open](open-method-ado-md.md) , чтобы повторно открыть набор **ячеек** с помощью той же или другой строки источника. Когда объект **Cell** закрывается, извлечение любых свойств или вызов методов, ссылающихся на базовые данные или метаданные, приводит к ошибке.

