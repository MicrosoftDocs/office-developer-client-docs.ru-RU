---
title: Свойство Direction (ADO)
TOCTitle: Direction property (ADO)
ms:assetid: 51a94abb-7ce9-9adb-2b76-5391eb9f6863
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249262(v=office.15)
ms:contentKeyID: 48544823
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 5885e89a3bce5d8b16ea855ce14689380655ad45
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293870"
---
# <a name="direction-property-ado"></a>Свойство Direction (ADO)


**Область применения**: Access 2013, Office 2013

Указывает, представляет [](parameter-object-ado.md) ли параметр входной параметр, выходной параметр, входной и выходной параметр, а также является ли параметр возвращаемой величиной из хранимой процедуры.

## <a name="settings-and-return-values"></a>Параметры и возвращаемые значения

Задает или возвращает значение [ParameterDirectionEnum.](parameterdirectionenum.md)

## <a name="remarks"></a>Заметки

Используйте свойство **Direction,** чтобы указать, как параметр передается процедуре или из нее. Свойство **Direction** имеет свойство read/write; Это позволяет работать с поставщиками, которые не возвращают эти сведения, или устанавливать эти сведения, если вы не хотите, чтобы ADO вызывался к поставщику для получения сведений о параметрах.

Не все поставщики могут определить направление параметров в хранимой процедуре. В таких случаях перед выполнением запроса необходимо установить свойство **Direction.**

