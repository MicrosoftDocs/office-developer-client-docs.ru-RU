---
title: Макрокоманда CancelRecordChange
TOCTitle: CancelRecordChange macro action
ms:assetid: 73031240-1ff6-660b-b25f-11a880df6031
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195846(v=office.15)
ms:contentKeyID: 48545626
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d19e7adcdd3bb60f24d90e75942fcc0b4e16e2e2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296656"
---
# <a name="cancelrecordchange-macro-action"></a>Макрокоманда CancelRecordChange


**Область применения**: Access 2013, Office 2013

Действие **CancelRecordChange** можно использовать для отмены изменений, примененных к записи в блоке данных **[CreateRecord](createrecord-data-block.md)** или **[EditRecord,](editrecord-data-block.md)** прежде чем изменения будут зафиксированы.


> [!NOTE]
> Действие **CancelRecordChange** доступно только в макросах данных.



## <a name="remarks"></a>Заметки

При вызове действия **CancelRecordChange** блок данных **CreateRecord** или **EditRecord** немедленно выходит из него.

