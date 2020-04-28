---
title: Свойство field2. OriginalValue (DAO)
TOCTitle: OriginalValue Property
ms:assetid: 10fed55e-c938-2ae6-8fd2-996745a63da3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845353(v=office.15)
ms:contentKeyID: 48543306
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1101183
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 3e3da5f7438ae83010c6ecc109dccf5d7a8eb9ef
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292743"
---
# <a name="field2originalvalue-property-dao"></a>Свойство field2. OriginalValue (DAO)


**Область применения**: Access 2013, Office 2013

## <a name="syntax"></a>Синтаксис

*Expression* . OriginalValue

*expression* — переменная, представляющая объект **Field2**.

## <a name="remarks"></a>Примечания

Во время оптимистического пакетного обновления может произойти конфликт, при котором второй клиент изменяет одно и то же поле и запись между моментом, когда первый клиент получает данные, и пытается выполнить обновление первого клиента. Свойство **originalValue** содержит значение поля во время последнего начала пакетного **обновления** . Если это значение не отвечает фактическому значению в базе данных при попытке пакетного **обновления** выполнить запись в базу данных, происходит конфликт. В этом случае новое значение в базе данных будет доступно через свойство **висиблевалуе** .

