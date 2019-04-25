---
title: Автоматизация в Microsoft Access
TOCTitle: Automation with Microsoft Access
description: Microsoft Access — это компонент COM, поддерживающий автоматизацию, которая ранее называлось автоматизацией OLE.
ms:assetid: 39fde349-3ba3-7c7a-3c92-316641dc8712
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192643(v=office.15)
ms:contentKeyID: 48544258
ms.date: 10/16/2018
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm13783
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: 9635cdb2a06f610f42e4aa9fc9f998719aebb986
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296964"
---
# <a name="automation-with-microsoft-access"></a>Автоматизация в Microsoft Access

**Область применения**: Access 2013, Office 2013

Microsoft Access — это компонент COM, поддерживающий автоматизацию, которая ранее называлось автоматизацией OLE. Microsoft Access поддерживает автоматизацию двумя способами. В Microsoft Access можно работать с объектами, предоставляемыми другими компонентами. Microsoft Access также предоставляет свои объекты в другие компоненты COM.

Можно использовать ключевое слово **New** или метод **CreateObject** для создания нового экземпляра компонента. Можно использовать метод **GetObject** для назначения переменной существующему экземпляру компонента.

В Microsoft Access можно задать ссылку на библиотеку типов компонента для повышения производительности при работе с этим компонентом с помощью автоматизации. Microsoft Access также содержит обозреватель объектов — средство, позволяющее просматривать объекты в библиотеке типов другого компонента, а также их методы и свойства.

Библиотека типов Microsoft Access предоставляет сведения об объектах Microsoft Access другим компонентам. Можно [задать ссылку](https://docs.microsoft.com/office/vba/access/Concepts/Settings/set-references-to-type-libraries) на библиотеку типов Microsoft Access из компонента и просматривать ее объекты в обозревателе объектов.

Для работы с объектами Microsoft Access с помощью автоматизации необходимо создать экземпляр объекта **[Application](https://docs.microsoft.com/office/vba/api/Access.Application)** приложения Microsoft Access. Например, если нужно отобразить данные из Microsoft Excel в форме или отчете Microsoft Access. Для запуска Microsoft Access из Microsoft Excel можно использовать ключевое слово **New**, чтобы создать экземпляр объекта **Application** приложения Microsoft Access. Вы также можете использовать метод **CreateObject**, чтобы создать новый экземпляр объекта **Application** приложения Microsoft Access, или метод **GetObject**, чтобы связать объектную переменную с существующим экземпляром Microsoft Access. Чтобы определить поддерживаемый синтаксис, см. документацию по своему компоненту.

После запуска экземпляра Microsoft Access, если нужно управлять любыми объектами Microsoft Access, потребуется открыть базу данных или проект (ADP) в окне Microsoft Access, воспользовавшись методом **[OpenCurrentDatabase](https://docs.microsoft.com/office/vba/api/Access.Application.OpenCurrentDatabase)** или **[NewCurrentDatabase](https://docs.microsoft.com/office/vba/api/Access.Application.NewCurrentDatabase)** для базы данных либо методом **[OpenAccessProject](https://docs.microsoft.com/office/vba/api/Access.Application.OpenAccessProject)** или **[NewAccessProject](https://docs.microsoft.com/office/vba/api/Access.Application.NewAccessProject)** для проекта.

Если вы открыли Microsoft Access только для использования объектов доступа к данным, предоставляемых DAO Майкрософт, не нужно открывать базу данных в окне Microsoft Access. Вы можете использовать свойство **[DBEngine](https://docs.microsoft.com/office/vba/api/Access.Application.DBEngine)** объекта **Application** приложения Microsoft Access для доступа к объектам в библиотеке объектов ядра СУБД Access Microsoft Office 12.0 во время операции автоматизации.

