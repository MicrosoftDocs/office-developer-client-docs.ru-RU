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

В COM большинство операций возвращают код возврата HRESULT, который указывает, успешно ли выполнена функция. Директива импорта создает код-оболочку для каждого "необработанных" метода или свойства и проверяет \# возвращенный HRESULT. Если HRESULT указывает на сбой, код-оболочка вызывает ошибку COM, вызывая \_ com \_ issue errorex() с кодом возврата HRESULT в качестве \_ аргумента. Объекты ошибки COM могут быть перехвачены в **блоке try-catch.** (Для повышения эффективности перехватить ссылку на объект \_ \_ ошибки com.)

Помните, что это ошибки ADO: они являются результатом сбоя операции ADO. Ошибки, возвращенные поставщиком, отображаются как **объекты Error** в коллекции **Errors объекта** **Connection.**

Директива импорта создает процедуры обработки ошибок только для методов и свойств, объявленных \# в DLL ADO. Однако вы можете воспользоваться этим же механизмом обработки ошибок, написав собственный макрос проверки ошибок или функцию. Примеры см. в разделе Visual C++ Extensions.

