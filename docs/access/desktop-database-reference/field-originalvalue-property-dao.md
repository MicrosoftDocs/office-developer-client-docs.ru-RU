---
title: Свойство Field.OriginalValue (DAO)
TOCTitle: OriginalValue Property
ms:assetid: 69ccec1e-311f-6905-e7bb-ad7fa8277494
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195384(v=office.15)
ms:contentKeyID: 48545418
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 95c2776e04497a1ac7f645659c7acc5d9eee2a63
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293002"
---
# <a name="fieldoriginalvalue-property-dao"></a>Свойство Field.OriginalValue (DAO)


**Область применения**: Access 2013, Office 2013

## <a name="syntax"></a>Синтаксис

*выражение .* OriginalValue

*выражение*: переменная, представляющая объект **Field**.

## <a name="remarks"></a>Примечания

Во время оптимистичного пакетного обновления может возникнуть конфликт, в котором второй клиент изменяет одно и то же поле и запись между моментом, когда первый клиент получает данные, и первой попыткой обновления клиента. Свойство **OriginalValue** содержит значение поля во время начала последнего пакета **обновления.** Если это значение не совпадает со значением  в базе данных при попытке пакетного обновления записать в базу данных, возникает конфликт. В этом случае новое значение в базе данных будет доступно через свойство **[VisibleValue.](field-visiblevalue-property-dao.md)**

