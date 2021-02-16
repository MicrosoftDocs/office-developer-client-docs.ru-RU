---
title: Применение шаблона образца поставщика
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: da487569-f2f0-404c-b944-38ed1c1b82bb
description: 'Примеры шаблонов поставщиков Outlook Social Connector (OSC) дают вам основу для реализации поставщика OSC. '
ms.openlocfilehash: 10fb21ab640e298bc655b8cad554fae789e2ad47
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425913"
---
# <a name="applying-a-sample-provider-template"></a>Применение шаблона образца поставщика

Примеры шаблонов поставщиков Outlook Social Connector (OSC) дают вам основу для реализации поставщика OSC. Шаблоны поставщиков доступны на C++, C# и Visual Basic. Эти шаблоны являются отправной точкой для разработки поставщика; Шаблоны не адресуют написание кода реализации для поставщика и создание пакета установки для поставщика. В следующей процедуре показано, как применить шаблон поставщика OSC при начале разработки поставщика.
  
### <a name="to-apply-an-osc-provider-template"></a>Применение шаблона поставщика OSC

1. В меню **"Пуск"** щелкните правой кнопкой **мыши Microsoft Visual Studio 2010** и выберите команду "Запуск **от** администратора". При запросе нажмите **кнопку "Да",** чтобы Visual Studio администратором. 
    
2. Измените имя проекта и пространство имен в шаблоне на идентификаторы имени проекта и пространства имен.
    
3. Измените **класс AssemblyInfo,** чтобы указать соответствующие сведения о сборке. 
    
4. Реализуйте члены интерфейса, **помеченные** как необходимые, и добавляйте дополнительные зависимости и ссылки при необходимости. 
    
5. Выполните построение проекта.
    
6. Убедитесь, что progID сборки поставщика указан в качестве ключа  `HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders` в .
    
7. Чтобы распространить проект установки, создайте проект установки в Visual Studio или средство установки по вашему выбору.
    
8. Проект установки должен завершить регистрацию COM для сборки, а также создать ключ ProgID, как указано в шаге 5.
    
## <a name="see-also"></a>См. также

- [Загрузка примеров](downloading-the-samples.md)
- [Примеры шаблонов OSC](osc-sample-templates.md)

