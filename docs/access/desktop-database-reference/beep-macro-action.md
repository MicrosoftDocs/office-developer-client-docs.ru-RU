---
title: Макрокоманда Beep (Справочник по базам данных Access на компьютере)
TOCTitle: Beep macro action
ms:assetid: 5ca1600f-7934-3b3d-19fd-f305cda0e5d8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194572(v=office.15)
ms:contentKeyID: 48545092
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm11853
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 96051d8389f4b8ba7005c75ccdb5e2780ba17138
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296866"
---
# <a name="beep-macro-action"></a>Макрокоманда Beep


**Область применения**: Access 2013, Office 2013

Вы можете использовать действие **Beep** для звукового сигнала в динамике компьютера.

## <a name="setting"></a>Параметр

В действии **Beep** нет аргументов.

## <a name="remarks"></a>Замечания

Вы можете использовать действие **Beep** для сигнализации следующих вхождений:

  - Возникли важные изменения экрана.

  - В элементе управления введен недопустимый тип данных. Например, пользователь ввел числовые данные в элемент управления "текстовое поле".

  - Макрос достиг определенной точки или выполнил действия.

Частота и продолжительность звукового сигнала зависят от аппаратного обеспечения, которое может различаться для разных компьютеров.

Чтобы запустить действие **Beep** в модуле Visual Basic для приложений (VBA), используйте метод **BEEPER** объекта **DoCmd** .

