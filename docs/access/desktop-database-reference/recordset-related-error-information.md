---
title: Сведения об ошибках, связанных с наборами записей
TOCTitle: Recordset-related error information
ms:assetid: 388308c7-e121-bd12-228a-312c897b8c55
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249136(v=office.15)
ms:contentKeyID: 48544222
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 12a67657d5543aac22a49690256b0410a2b901bd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307618"
---
# <a name="recordset-related-error-information"></a>Сведения об ошибках, связанных с наборами записей

**Область применения**: Access 2013, Office 2013

Во время пакетной обработки свойство **Status** объекта **Recordset** предоставляет сведения об отдельных записЯх в **наборе записей**. Перед пакетным обновлением в свойстве **Status** объекта **Recordset** отображаются сведения о записях, которые необходимо добавить, изменить и удалить. 

После вызова **UpdateBatch** свойство **Status** указывает на успешное или неудачное выполнение операции. При переходе от записи к записи в **наборе записей** значение свойства **Status** изменяется, чтобы описать состояние текущей записи.

