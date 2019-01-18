---
title: Автоматизация в Microsoft Access
TOCTitle: Automation with Microsoft Access
description: Microsoft Access — это COM-компонентом, который поддерживает автоматизацию, ранее — OLE-автоматизации.
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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28716028"
---
# <a name="automation-with-microsoft-access"></a>Автоматизация в Microsoft Access

**Применимо к**: Access 2013, Office 2013

Microsoft Access — это COM-компонентом, который поддерживает автоматизацию, ранее — OLE-автоматизации. Microsoft Access поддерживает автоматизацию двумя способами. В Microsoft Access можно работать с объектами, предоставленного другим компонентом. Microsoft Access также предоставляет его объекты на другие COM-компоненты.

Чтобы создать новый экземпляр объекта компонента можно использовать ключевое слово **New** или метод **CreateObject** . Метод **GetObject** переменную назначить существующий экземпляр компонента.

В Microsoft Access можно задать ссылку на библиотеку типов компонента для повышения производительности при работе с этим компонентом через средство автоматизации. Microsoft Access также включает в себя обозреватель объектов, это средство, которое позволяет просматривать объекты в другой компонент библиотеки типов, а также их методы и свойства.

Библиотека типов Microsoft Access предоставляет сведения об объектах Microsoft Access для других компонентов. Можно [задать ссылку](https://docs.microsoft.com/office/vba/access/Concepts/Settings/set-references-to-type-libraries) для Microsoft Access введите библиотеки из компонента и просмотреть его объектов в обозревателе объектов.

Для работы с Microsoft Access объектов с помощью автоматизации, необходимо создать экземпляр объекта Microsoft Access **[приложения](https://docs.microsoft.com/office/vba/api/Access.Application)** . Например предположим, что требуется для отображения данных из Microsoft Excel в Microsoft Access форму или отчет. Для запуска Microsoft Access из Microsoft Excel, можно использовать ключевое слово **New** для создания экземпляра объекта Microsoft Access **приложения** . Можно также использовать метод **CreateObject** для создания нового экземпляра объекта Microsoft Access **приложения** , или можно использовать метод **GetObject** для указания объектную переменную на существующий экземпляр Microsoft Access. Проверьте документацию вашего компонента, чтобы определить, какой синтаксис, он поддерживает.

После запуска экземпляра Microsoft Access, если вы хотите управлять любые объекты Microsoft Access, необходимо открыть базу данных или проектов (файлы с расширением ADP) в окне Microsoft Access с помощью **[OpenCurrentDatabase](https://docs.microsoft.com/office/vba/api/Access.Application.OpenCurrentDatabase)** или **[NewCurrentDatabase ](https://docs.microsoft.com/office/vba/api/Access.Application.NewCurrentDatabase)** метод для базы данных или с помощью **[OpenAccessProject](https://docs.microsoft.com/office/vba/api/Access.Application.OpenAccessProject)** или метод **[NewAccessProject](https://docs.microsoft.com/office/vba/api/Access.Application.NewAccessProject)** для проекта.

При открытии Microsoft Access только с точки зрения с помощью объекты доступа к данным, предоставляемые Майкрософт DAO не требуется открывать базу данных в окне Microsoft Access. Можно использовать свойство **[DBEngine](https://docs.microsoft.com/office/vba/api/Access.Application.DBEngine)** объекта Microsoft Access **приложения** для доступа к объектам в библиотеке объектов модуля Microsoft Office 12.0 доступа к базе данных во время операции автоматизации.

