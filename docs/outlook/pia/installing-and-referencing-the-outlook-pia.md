---
title: Установка и создание ссылок на Outlook PIA
TOCTitle: Installing and referencing the Outlook PIA
ms:assetid: b1afd047-dcbb-480f-ba74-993d7d7114cb
ms:mtpsurl: https://msdn.microsoft.com/library/office/bb646840(v=office.15)
ms:contentKeyID: 55119774
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 45584ae0a7050aa769368db518c9efcd5db9975a
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28718205"
---
# <a name="installing-and-referencing-the-outlook-pia"></a>Установка и создание ссылок на Outlook PIA

Необходимо установить основную сборку взаимодействия с Outlook (PIA) в глобальный кэш сборок (GAC), чтобы включить информацию из PIA в управляемую надстройку Outlook. По умолчанию PIA автоматически устанавливается при установке Office на компьютере для разработки. Если нужно установить PIA отдельно, см. статью [Настройка компьютера для разработки решений Office](https://docs.microsoft.com/visualstudio/vsto/configuring-a-computer-to-develop-office-solutions?view=vs-2017).


> [!NOTE] 
> Необходимо быть администратором на компьютере для разработки, чтобы установить Office PIA.

Если после установки для создания управляемого проекта используется Visual Studio, можно добавить ссылку на компонент Microsoft Outlook 15.0 Object Library. Затем в пространстве имен **Microsoft.Office.Interop.Outlook** обозревателя объектов можно увидеть управляемые интерфейсы в PIA, имена которых соответствуют объектам в объектной модели Outlook.

## <a name="see-also"></a>См. также

- [Установка основных сборок взаимодействия Office](https://docs.microsoft.com/visualstudio/vsto/how-to-install-office-primary-interop-assemblies?view=vs-2017)
- [Архитектура Outlook PIA](architecture-of-the-outlook-pia.md)

