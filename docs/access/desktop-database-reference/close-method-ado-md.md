---
title: Close Method (ADO MD)
TOCTitle: Close Method (ADO MD)
ms:assetid: 683788b0-0a96-a165-6b49-8d7036850756
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249406(v=office.15)
ms:contentKeyID: 48545382
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 39059a684a2a64574fc270f3fbd3797a00f66b96
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25482951"
---
# <a name="close-method-ado-md"></a>Close Method (ADO MD)


**Применимо к**: Access 2013 | Office 2013

Закрытие открытых ячеек.

## <a name="syntax"></a>Синтаксис

*Набор ячеек*. Закрыть

## <a name="remarks"></a>Замечания

С помощью метода **Закрыть** для закрытия объекта [ячеек](cellset-object-ado-md.md) выпустит связанных данных, включая данные в связанные [ячейки](cell-object-ado-md.md), [ось](axis-object-ado-md.md), [положение](position-object-ado-md.md)или [член](member-object-ado-md.md) объекты. Закрытие **ячеек** не удаляется из памяти; можно изменить параметры его свойств и откройте его позже. Чтобы полностью удалить объект из памяти, задайте объектной переменной значение **Nothing**.

Позднее можно вызвать метод [Open](open-method-ado-md.md) , и снова откройте **ячеек** , с помощью того же или другой источник строки. При закрытии объекта **ячеек** , извлечение всех свойств или вызов любых методов, ссылающиеся на базовой данных или метаданных приводит к ошибке.

