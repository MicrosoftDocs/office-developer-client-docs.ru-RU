---
title: Обработка ошибок в Visual C++
TOCTitle: Handling errors in Visual C++
ms:assetid: 75e15699-0c84-1dca-654e-f9ac465c2a30
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249483(v=office.15)
ms:contentKeyID: 48545684
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d0e76dc3cc9634a1531a34058bf7a1baf636c94c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292029"
---
# <a name="handling-errors-in-visual-c"></a>Обработка ошибок в Visual C++


**Область применения**: Access 2013, Office 2013

В com большинство операций возвращают код возврата HRESULT, который указывает, успешно ли выполнена функция. Директива импорта создает код оболочки вокруг каждого "необработанных" метода или свойства и проверяет \# возвращаемую HRESULT. Если HRESULT указывает на сбой, код оболочки вызывает ошибку COM, вызывая ошибку com issue errorex() с кодом возврата \_ \_ HRESULT в качестве \_ аргумента. Объекты ошибки COM могут быть пойманы в **блоке try-catch.** (Для обеспечения эффективности ловите ссылку на объект \_ ошибки \_ com.)

Помните, что это ошибки ADO: они являются результатом сбоя операции ADO. Ошибки, возвращаемые поставщиком, отображаются как **объекты ошибки** в коллекции **Ошибок** объекта **Подключения.**

Директива импорта создает только процедуры обработки ошибок для методов и свойств, объявленных в \# ADO .dll. Однако вы можете воспользоваться этим же механизмом обработки ошибок, написав собственную макрос или функцию inline для проверки ошибок. Примеры см. в разделе Visual C++ Extensions.

