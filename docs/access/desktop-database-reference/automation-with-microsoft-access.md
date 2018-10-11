---
title: Automation with Microsoft Access
TOCTitle: Automation with Microsoft Access
ms:assetid: 39fde349-3ba3-7c7a-3c92-316641dc8712
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192643(v=office.15)
ms:contentKeyID: 48544258
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm13783
f1_categories:
- Office.Version=v15
ms.openlocfilehash: bd0e230d2b4c31d497e913e8e1ccf4d2172402e9
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25481785"
---
# <a name="automation-with-microsoft-access"></a>Automation with Microsoft Access


**Применимо к**: Access 2013 | Office 2013

Microsoft Access — это COM-компонентом, который поддерживает автоматизацию, ранее — OLE-автоматизации. Microsoft Access поддерживает автоматизацию двумя способами. В Microsoft Access можно работать с объектами, предоставленного другим компонентом. Microsoft Access также предоставляет его объекты на другие COM-компоненты.

Чтобы создать новый экземпляр объекта компонента можно использовать ключевое слово **New** или метод **CreateObject** . Метод **GetObject** переменную назначить существующий экземпляр компонента.

В Microsoft Access можно задать ссылку на библиотеку типов компонента для повышения производительности при работе с этим компонентом через средство автоматизации. Microsoft Access также включает в себя обозреватель объектов, это средство, которое позволяет просматривать объекты в другой компонент библиотеки типов, а также их методы и свойства.

Библиотека типов Microsoft Access предоставляет сведения об объектах Microsoft Access для других компонентов. Можно [задать ссылку](https://msdn.microsoft.com/library/ff194944\(v=office.15\)) для Microsoft Access введите библиотеки из компонента и просмотреть его объектов в обозревателе объектов.

Для работы с Microsoft Access объектов с помощью автоматизации, необходимо создать экземпляр объекта Microsoft Access **[приложения](https://msdn.microsoft.com/library/ff821758\(v=office.15\))** . Например предположим, что требуется для отображения данных из Microsoft Excel в Microsoft Access форму или отчет. Для запуска Microsoft Access из Microsoft Excel, можно использовать ключевое слово **New** для создания экземпляра объекта Microsoft Access **приложения** . Можно также использовать метод **CreateObject** для создания нового экземпляра объекта Microsoft Access **приложения** , или можно использовать метод **GetObject** для указания объектную переменную на существующий экземпляр Microsoft Access. Проверьте документацию вашего компонента, чтобы определить, какой синтаксис, он поддерживает.

После запуска экземпляра Microsoft Access, если вы хотите управлять любые объекты Microsoft Access, необходимо открыть базу данных или проектов (файлы с расширением ADP) в окне Microsoft Access с помощью **[OpenCurrentDatabase](https://msdn.microsoft.com/library/ff837226\(v=office.15\))** или **[NewCurrentDatabase ](https://msdn.microsoft.com/library/ff195271\(v=office.15\))** метод для базы данных или с помощью **[OpenAccessProject](https://msdn.microsoft.com/library/ff837249\(v=office.15\))** или метод **[NewAccessProject](https://msdn.microsoft.com/library/ff835758\(v=office.15\))** для проекта.

При открытии Microsoft Access только с точки зрения с помощью объекты доступа к данным, предоставляемые Майкрософт DAO не нужно открыть базу данных в окне Microsoft Access. Можно использовать свойство **[DBEngine](https://msdn.microsoft.com/library/ff821724\(v=office.15\))** объекта Microsoft Access **приложения** для доступа к объектам в библиотеку объектов модуль библиотеки объектов 12.0 доступа Microsoft Office базы данных во время операции автоматизации.

