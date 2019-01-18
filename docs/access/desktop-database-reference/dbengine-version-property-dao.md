---
title: Свойство DBEngine.Version (DAO)
TOCTitle: Version Property
ms:assetid: b2807dc1-604f-4423-289a-ff38a3d9f31b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822024(v=office.15)
ms:contentKeyID: 48547171
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052986
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 7e22645127f18ad815c398fd38f9ac4615dfadc9
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28712787"
---
# <a name="dbengineversion-property-dao"></a>Свойство DBEngine.Version (DAO)


**Применимо к**: Access 2013, Office 2013

Возвращает версию DAO в настоящее время используется. Только для чтения, **String**.

## <a name="syntax"></a>Синтаксис

*выражение* . Версия

*выражение* Переменная, которая представляет собой объект- **DBEngine** .

## <a name="remarks"></a>Замечания

Возвращаемое значение — это строка, которое оценивается как номер версии в форме «major.minor». Например «3.0». Номер версии продукта состоит из номера версии (3), за период и номер версии (0).

