---
title: Устранение неполадок шаблонов форм, использующих объектную модель InfoPath во время выполнения
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- troubleshooting form templates [infopath 2007], run time,InfoPath 2003-compatible form templates, troubleshooting at run time
localization_priority: Normal
ms.assetid: 65e7882e-6397-4375-9bb4-d993d700d749
description: В следующих разделах описаны типичные сценарии устранения неполадок, которые могут встретиться при работе с шаблонами форм InfoPath с управляемым кодом, использующими объектную модель, совместимую с InfoPath 2003 и предоставляемую пространством имен Microsoft.Office.Interop.InfoPath.SemiTrust во время выполнения.
ms.openlocfilehash: 8c83679a0cd61fae212b3143b6b0131da92ac7f9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807599"
---
# <a name="troubleshoot-form-templates-that-use-the-infopath-object-model-at-run-time"></a>Устранение неполадок шаблонов форм, использующих объектную модель InfoPath во время выполнения

В следующих разделах описаны типичные сценарии устранения неполадок, которые могут встретиться при работе с шаблонами форм InfoPath с управляемым кодом, использующими объектную модель, совместимую с InfoPath 2003 и предоставляемую пространством имен **Microsoft.Office.Interop.InfoPath.SemiTrust** во время выполнения. 
  
## <a name="display-notifications-for-unhandled-managed-code-exceptions-at-run-time"></a>Отображение уведомлений о необработанных исключений управляемого кода во время выполнения

Если в коде формы не используется обработка исключений "try-catch", то при отладке и просмотре приложение InfoPath будет отображать сведения о необработанных исключениях в диалоговом окне ошибок InfoPath. Однако по умолчанию необработанные исключения не отображаются в диалоговом окне InfoPath во время выполнения при развертывании шаблона формы с управляемым кодом.. Если вы хотите исключений управляемого кода, отображаемые во время выполнения, выполните процедуру, описанную в разделе «Обработка управляемого кода исключения» [Обработки ошибок с помощью объектной модели InfoPath 2003](how-to-handle-errors-using-the-infopath-2003-object-model.md).
  
## <a name="problems-with-managed-code-form-templates-after-deployment"></a>Проблемы с шаблонами форм с управляемым кодом после развертывания

Убедитесь, что для тестирования шаблона форм с управляемым кодом в расположение, где он будет наконец развернут. Процедуры развертывания содержатся в разделе [Развертывание шаблонов форм InfoPath с кодом](how-to-deploy-infopath-form-templates-with-code.md). Сведения о сценариях безопасности, влияющие на развертывание содержатся в разделе [О модели безопасности для шаблонов форм с кодом](about-the-security-model-for-form-templates-with-code.md).
  
При использовании служебной программы настройки .NET Framework 1.1 и группы кода шаблонов форм InfoPath для добавления определенных разрешений для шаблонов форм с управляемым кодом, убедитесь в том, что та же политика безопасности будет развернуто на всех клиентских компьютерах. Кроме того, при указании **URLEvidence** , на который ссылается на расположение на локальном компьютере, убедитесь в том, что указанное место относится к папке, где будет решения и, наконец развернут (не же расположение используется во время разработки). Сведения о настройке параметров безопасности .NET Framework для шаблонов форм с управляемым кодом см в разделе «Назначение FullTrust для форм в конкретных URL-адрес или UNC-пути» в разделе [Настройка параметров безопасности для шаблонов форм с кодом](how-to-configure-security-settings-for-form-templates-with-code.md) . 
  
## <a name="see-also"></a>См. также

- [Модель безопасности для шаблонов форм с кодом](about-the-security-model-for-form-templates-with-code.md)
- [Развертывание шаблонов форм InfoPath с кодом](how-to-deploy-infopath-form-templates-with-code.md)
- [Обработка ошибок с помощью объектной модели InfoPath 2003](how-to-handle-errors-using-the-infopath-2003-object-model.md)
- [Отладка проектов InfoPath с помощью объектной модели InfoPath 2003](how-to-debug-infopath-projects-using-the-infopath-2003-object-model.md)

