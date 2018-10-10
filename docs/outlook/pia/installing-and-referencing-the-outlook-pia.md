---
title: Установка и создание ссылок на Outlook PIA
TOCTitle: Installing and referencing the Outlook PIA
ms:assetid: b1afd047-dcbb-480f-ba74-993d7d7114cb
ms:mtpsurl: https://msdn.microsoft.com/library/office/bb646840(v=office.15)
ms:contentKeyID: 55119774
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 42e79fcd6cf9575f43722d7ba467b028ef6c3e16
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25405513"
---
# <a name="installing-and-referencing-the-outlook-pia"></a>Установка и создание ссылок на Outlook PIA

Необходимо установить основную сборку взаимодействия с Outlook (PIA) в глобальный кэш сборок (GAC), чтобы включить информацию из PIA в управляемую надстройку Outlook. По умолчанию PIA автоматически устанавливается при установке Office на компьютере для разработки. Если нужно установить PIA отдельно, см. статью [Настройка компьютера для разработки решений Office](https://docs.microsoft.com/visualstudio/vsto/configuring-a-computer-to-develop-office-solutions?view=vs-2017).


> [!NOTE] 
> Необходимо быть администратором на компьютере для разработки, чтобы установить Office PIA.

Если после установки для создания управляемого проекта используется Visual Studio, можно добавить ссылку на компонент Microsoft Outlook 15.0 Object Library. Затем в пространстве имен **Microsoft.Office.Interop.Outlook** обозревателя объектов можно увидеть управляемые интерфейсы в PIA, имена которых соответствуют объектам в объектной модели Outlook.

## <a name="see-also"></a>См. также

- [Установка основных сборок взаимодействия Office](https://docs.microsoft.com/visualstudio/vsto/how-to-install-office-primary-interop-assemblies?view=vs-2017)
- [Архитектура Outlook PIA](architecture-of-the-outlook-pia.md)

