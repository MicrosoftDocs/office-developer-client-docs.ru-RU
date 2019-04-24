---
title: Архитектура Outlook PIA
TOCTitle: Architecture of the Outlook PIA
ms:assetid: 89577d14-e6e2-4270-8e72-b0adba378667
ms:mtpsurl: https://msdn.microsoft.com/library/office/bb646255(v=office.15)
ms:contentKeyID: 55119777
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 37ecad42b08b96d79d96d62f98e27913a0309971
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336528"
---
# <a name="architecture-of-the-outlook-pia"></a>Архитектура Outlook PIA

Основная сборка взаимодействия Outlook (PIA) полностью поддерживает разработку управляемого кода с использованием объектной модели Outlook. Но при первом взгляде на PIA в обозревателе объектов можно удивиться обилию лишних интерфейсов, содержащихся в PIA, и тому факту, что не все члены  методы, свойства и события  объекта представлены одним и тем же интерфейсом объекта. Подразделы этого раздела содержат указания по доступу из кода к членам объектов, а также по поиску справки для объектов, методов, свойств и событий.

## <a name="in-this-section"></a>В этой статье

|Статья|Описание|
|:----|:----------|
|[Связывание Outlook PIA с объектной моделью](relating-the-outlook-pia-with-the-object-model.md) |Описывает порядок сопоставления объектов и элементов объектной модели Outlook на основе COM соответствующим управляемым интерфейсам и классам PIA.|
|[Объекты в Outlook PIA](objects-in-the-outlook-pia.md) |Описывает типовые интерфейсы, классы и делегаты .NET, сопоставляемые с COM-объектом, а также описывает доступ к объекту в PIA.|
|[Методы и свойства в Outlook PIA](methods-and-properties-in-the-outlook-pia.md) |Описывает, как получить доступ к методам и свойствам объекта в управляемом коде с помощью PIA.|
|[События в Outlook PIA](events-in-the-outlook-pia.md) |Описывает интерфейсы, связанные с событиями, делегаты и классы модуля поддержки приемника в PIA.|

## <a name="see-also"></a>См. также

- [Подготовка использования Outlook PIA](setting-up-to-use-the-outlook-pia.md)
- [Разработка управляемых надстроек для Outlook с помощью Outlook PIA](developing-managed-outlook-add-ins-using-the-outlook-pia.md)
- [Инструкции (справочник по основной сборке взаимодействия для Outlook 2013)](how-do-i-outlook-2013-pia-reference.md)

