---
title: DBEngine.Version Property (DAO)
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
ms.openlocfilehash: 865942cdf4cca81cb0d5348725164a4a75a845fb
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25870914"
---
# <a name="dbengineversion-property-dao"></a>DBEngine.Version Property (DAO)


**Применимо к**: Access 2013, Office 2013

Возвращает версию DAO в настоящее время используется. Только для чтения, **String**.

## <a name="syntax"></a>Синтаксис

*выражение* . Версия

*выражение* Переменная, которая представляет собой объект- **DBEngine** .

## <a name="remarks"></a>Замечания

Возвращаемое значение — это строка, которое оценивается как номер версии в форме «major.minor». Например «3.0». Номер версии продукта состоит из номера версии (3), за период и номер версии (0).

