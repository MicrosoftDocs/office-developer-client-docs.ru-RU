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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294192"
---
# <a name="dbengineversion-property-dao"></a>Свойство DBEngine.Version (DAO)


**Область применения**: Access 2013, Office 2013

Rreturns версия DAO в настоящее время используется. Только для чтения, **String**.

## <a name="syntax"></a>Синтаксис

*выражения* . Версия

*expression*: переменная, представляющая объект **DBEngine**.

## <a name="remarks"></a>Примечания

Возвращаемая величина — это строка, которая оценивает номер версии в форме "major.minor". Например, "3.0". Номер версии продукта состоит из номера версии (3), периода и номера выпуска (0).

