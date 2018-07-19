---
title: Знакомство с пакетом средств разработки программного обеспечения для Excel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- excel 2007 xll software development kit,add-ins [Excel 2007]
localization_priority: Normal
ms.assetid: abfc9d76-6f22-49b9-ba45-eb7a54b082e0
description: 'Относится к: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 4de88a12b5fb945c6243e52b77babe88b2d02417
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807331"
---
# <a name="welcome-to-the-excel-software-development-kit"></a>Знакомство с пакетом средств разработки программного обеспечения для Excel

 **Относится к**: Excel 2013 | Office 2013 | Visual Studio 
  
Добро пожаловать в документацию по пакету средств разработки (SDK) XLL для Excel 2013. Этот справочник включает концептуальные обзоры, задачи программирования и примеры, которые помогут вам разрабатывать XLL для Microsoft Excel 2013.
  
Последняя редакция: ноябрь 2012 г.
  
Скачайте [пакет SDK XLL для Excel 2013](http://go.microsoft.com/fwlink/?LinkID=251082&amp;clcid=0x409).
  
Пакет SDK XLL для Excel 2013 включает следующее:
  
- **Программный интерфейс (API) C** включает файлы заголовков и исходные файлы, которые позволяют библиотекам DLL получать доступ к функциям Excel 2013, и описание интерфейса, который библиотека DLL должна предоставлять для работы с диспетчером надстроек Excel.
    
- **Проекты Microsoft Visual Studio** включают исходный код на C/C++ и демонстрируют использование API C. Эти примеры проектов включают примеры кода и служат отправной точкой для разработки собственных надстроек.
    
Документация по SDK включает следующие разделы:
  
- [Начало работы с пакетом SDK XLL для Excel](getting-started-with-the-excel-xll-sdk.md)
    
- [Разработка XLL-файлов для Excel](developing-excel-xlls.md)
    
- [Разработка соединителей кластеров Excel](developing-excel-cluster-connectors.md)
    
- [Справочник по функциям API SDK XLL для Excel](excel-xll-sdk-api-function-reference.md)
    
## <a name="functionality-not-covered"></a>Не рассмотренные функции

Не рассматриваются следующие темы:
  
- Разработка определенных пользователем функций и команд в листах макросов Excel (XLM).
    
- Создание определенных пользователем функций в библиотеках DLL, которые управляют потоком выполнения макроса XLM.
    
    Такие функции работают, возвращая специальный тип данных элемента управления потоком, который также не описываются в данной документации.
    
## <a name="related-links"></a>Дополнительные ссылки

[Центр разработчиков Excel](http://msdn.microsoft.com/ru-RU/office/aa905411.aspx)
  
[Центр разработчика Microsoft Office](http://msdn.microsoft.com/ru-RU/office/default.aspx)
  
[Пакет SDK для Excel 2010: пакет средств разработки XLL для Excel 2010](http://go.microsoft.com/fwlink/?LinkID=186435&amp;clcid=0x409)
  

