---
title: О модели безопасности шаблонов форм с кодом
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- infopath 2007, security,code access security [InfoPath 2007],security [InfoPath 2007], security model for managed code,security [InfoPath 2007], levels,CAS [InfoPath 2007],InfoPath 2003-compatible form templates, security,permissions [InfoPath 2007]
localization_priority: Normal
ms.assetid: 5e1c1c72-f98d-4871-9c57-82c315277aa1
description: Шаблоны форм InfoPath с управляемым кодом поддерживают такие же уровни безопасности, как и скрипт, выполняющийся в неуправляемых шаблонах форм. Они также поддерживают дополнительные возможности доступа к коду, которые применяются к управляемому коду, работающему в среде CLR платформы .NET Framework.
ms.openlocfilehash: 97f0239a5bd6699b539ddaebf4d1d2ed7d1394db
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436148"
---
# <a name="about-the-security-model-for-form-templates-with-code"></a>О модели безопасности шаблонов форм с кодом

Шаблоны форм InfoPath с управляемым кодом поддерживают такие же уровни безопасности, как и скрипт, выполняющийся в неуправляемых шаблонах форм. Они также поддерживают дополнительные возможности доступа к коду, которые применяются к управляемому коду, работающему в среде CLR платформы .NET Framework.
  
## <a name="infopath-managed-object-model-security-levels"></a>Уровни безопасности объектной модели InfoPath с управляемым кодом

В следующей таблице описаны соотношения различных уровней безопасности для элементов объектной модели скрипта, а также соответствующий набор разрешений, необходимый для каждого уровня при использовании элемента объектной модели в шаблоне формы с управляемым кодом.
  
|**Уровень безопасности объектной модели**|**Описание**|**Необходимый набор разрешений**|
|:-----|:-----|:-----|
|0  <br/> |Доступ возможен без ограничений.  <br/> |Нет  <br/> |
|2  <br/> |Доступ возможен только от форм, запущенных на том же домене, что и открытая в данный момент форма, либо от форм, которым были присвоены междоменные разрешения.  <br/> |Нет  <br/> |
|3  <br/> |Доступ возможен только от форм с полным доверием.  <br/> |FullTrust  <br/> |
   
> [!NOTE]
> Уровень безопасности "1" не используется текущим сервером COM приложения InfoPath и зарезервирован для использования в будущем. 
  
> [!IMPORTANT]
> [!Важно!] Несмотря на то, что уровни 0 и 2 в объектной модели не требуют какого-либо набора разрешений, поскольку содержат управляемый код, они рассматриваются как определенные на уровне безопасности "Домен" для доступа к доменам, как описано в следующем разделе. 
  
Уровень безопасности каждого элемента объектной модели, предоставляемого сборками Microsoft.Office.InfoPath и Microsoft.Office.Interop.InfoPath.SemiTrust, указан в разделе "Заметки" темы с документацией по этому элементу в пространствах имен [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) и [Microsoft.Office.Interop.InfoPath.SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) . 
  
## <a name="infopath-domain-access-security-levels"></a>Уровни безопасности доступа к доменам InfoPath

В сочетании с уровнями безопасности объектной модели, которые применяются сервером COM, предоставляемым приложением InfoPath, в приложении InfoPath также определяются три уровня безопасности, которые применяются в зависимости от местоположения шаблона формы, метода развертывания формы и параметров, настроенных в режиме конструктора. Эти три уровня безопасности описаны в следующей таблице.
  
|**Уровень безопасности доступа к доменам**|**Описание**|
|:-----|:-----|
|Restricted  <br/> |Полностью запрещает внешние связи шаблона формы. Этот уровень безопасности призван предотвратить любую возможную передачу данных вредоносными формами от текущего компьютера к злоумышленнику. При работе в этом режиме безопасности не будут работать следующие функции: настраиваемая области задач, подключения к данным (за исключением отправки электронной почты), элементы управления ActiveX, управляемый код формы кода, роли и рабочий процесс. Шаблоны форм с управляемым кодом невозможно запустить на домене с доступом "Ограниченный". Если для шаблона формы с управляемым кодом установлен параметр **Автоматически определять уровень безопасности** в категории **Безопасность и доверие** диалогового окна **Параметры формы**, шаблону формы для запуска кода всегда будет необходим как минимум уровень доступа безопасности "Домен".  <br/><br/>**ВАЖНО:** сборка управляемого кода, созданная для шаблона управляемых форм кода, не загружается и не будет работать, когда форма открывается из ограниченного домена, например из формы InfoPath, отправленной в виде вложения электронной почты. Любой шаблон формы, который вы хотите развернуть в качестве вложения электронной почты, должен опустить указанные выше функции, и если шаблон формы содержит код формы, код формы должен быть реализован в JScript или VBScript и должен использовать только участников объектной модели с уровнем безопасности 0 (ноль).           |
|Домен  <br/> |Ограничивает форму на основе ее размещения в одной из зон безопасности, указанных приложением Microsoft Internet Explorer. Например, если форма расположена в зоне "Местная интрасеть", то ей разрешено связываться с другими данными вне исходного домена, но не разрешено получать данные из других доменов. Размещение в зоне безопасности Microsoft Internet Explorer также определяет разрешение на запуск элементов управления ActiveX, отмеченных как небезопасные для скриптов.  <br/> |
|Полное доверие  <br/> |Позволяет запускать форму с полным доверием на том компьютере, где будет использоваться форма. Этот уровень безопасности можно использовать только при работе с формами, имеющими цифровую подпись, соответствующую надежному корневому издателю на данном компьютере, либо при создании программы установки, которая устанавливает форму и задает для атрибута **requireFullTrust** элемента **xDocumentClass** значение "yes" в файле определения формы (.xsf). Используя этот параметр, форма может получать доступ к объектной модели, вызывающей необходимый уровень безопасности объектной модели 3, в частности свойства и методы, использующие доступ к файловой системе. Также при этом можно отключить определенные запросы безопасности, которые выводятся при запуске на более ограниченном уровне безопасности. <br/> |
   
По умолчанию форма InfoPath настраивается для автоматического выбора уровня безопасности с ограниченным доступом или домена в зависимости от функций, используемых в шаблоне формы, а также места развертывания шаблона формы. Например, шаблон формы, развернутый в виде вложения электронной почты, автоматически настраивается на уровень безопасности с ограниченным доступом. Параметр безопасности всегда является максимально ограничительным, начиная с Restricted, чтобы обеспечить более высокий уровень защиты для вас и ваших данных. Если шаблон формы, содержащий управляемый код, будет автоматически выбирать уровень безопасности, шаблон формы всегда будет требовать по крайней мере уровня доступа к безопасности домена перед запуском кода. Вы можете вручную переопрепредить этот параметр во время разработки, чтобы выбрать уровень безопасности, более подходящий для формы, с помощью следующей процедуры. 
  
### <a name="specify-a-forms-security-level"></a>Указание уровня безопасности формы

1. Откройте форму в разработчике форм InfoPath, щелкните вкладку **Файл**, нажмите **Сведения**, а затем выберите **Параметры формы**.
    
2. В диалоговом окне **Параметры формы** выберите категорию **Безопасность и доверие**. 
    
3. Снимите флажок **Автоматически определять уровень безопасности (рекомендуется)**. 
    
4. Выберите необходимый уровень безопасности.
    
> [!NOTE] 
> - Если для шаблона формы с управляемым кодом выбрать уровень безопасности **Ограниченный**, то код формы не будет загружаться и запускаться независимо от того, какие элементы объектной модели используются в этом коде. Этот уровень безопасности в первую очередь предназначен для форм InfoPath, развернутых с помощью электронной почты.     
> - Если выбрать уровень безопасности **Полное доверие**, то необходимо поставить цифровую подпись или установить и зарегистрировать формы. Дополнительные сведения см. в [тексте Развертывание шаблонов форм InfoPath с кодом.](how-to-deploy-infopath-form-templates-with-code.md)
    
В следующей таблице содержатся обобщенные сведения о модели безопасности InfoPath. В первом столбце перечислены уровни, указываемые или требующиеся для формы. Во втором и третьем столбцах указывается наличие идентификатора URN или URL для расположения формы. В остальных столбцах указываются объекты, запуск которых разрешен. Дополнительные сведения о скриптах развертывания и наборах разрешений для шаблонов форм с управляемым кодом см. в разделе "Функции безопасности для доступа к коду в среде CLR" далее в этой теме.
  
|**Уровень, необходимый для формы**|**Наличие идентификатора URN**|**Наличие идентификатора URL**|**Отметка небезопасности ActiveX для скриптов**|**Меж доменный доступ**|**Управляемый код**|**Безопасность объектной модели**|
|:-----|:-----|:-----|:-----|:-----|:-----|:-----|
|Restricted  <br/> ||X  <br/> |Нет ActiveX для всех  <br/> |Fail  <br/> |Ферма загружается, но управляемый код не запускается.  <br/> |0  <br/> |
|Домен (Зона **Ограниченные узлы** в Internet Explorer)  <br/> |Не запускается для всех  <br/> |Не запускается для всех  <br/> |Не запускается для всех  <br/> |Не запускается для всех  <br/> |Не запускается для всех  <br/> |Не запускается для всех  <br/> |
|Домен (зона **Интернет** в Internet Explorer)  <br/> |X  <br/> ||Fail  <br/> |Fail  <br/> |Не запускается для всех  <br/> |0  <br/> |
|Домен (зона **Местная интрасеть** Internet Explorer)  <br/> |X  <br/> ||Fail  <br/> |Prompt  <br/> |Управляемый код запускается с разрешениями **Местная интрасеть**.  <br/> |2  <br/> |
|Домен (зона **Надежные узлы** в Internet Explorer)  <br/> |X  <br/> ||Prompt  <br/> |OK  <br/> |Управляемый код запускается с разрешениями **Интернет**. Междоменный доступ разрешен. Обратите внимание, что даже если форма находится в зоне **Надежные узлы**, то применяются разрешения зоны **Интернет**.<br/> |2  <br/> |
|Домен (зона **Локальный компьютер** в Internet Explorer)  <br/> |X  <br/> |X  <br/> |Prompt  <br/> |Fail  <br/> |Управляемый код запускается с разрешениями **Местная интрасеть**.  <br/> |2  <br/> |
|Полное доверие  <br/> |X  <br/> |X  <br/> |OK  <br/> |OK  <br/> |Полное доверие  <br/> |3  <br/> |
   
> [!IMPORTANT]
> Приведенные выше описания в столбцах "Отметка небезопасности ActiveX для скриптов" и "Междоменный доступ" предполагают использование параметров безопасности Microsoft Internet Explorer по умолчанию. Если пользователь изменяет эти параметры безопасности, то поведение InfoPath изменится соответствующим образом. Например, если в зоне **Местная интрасеть** для параметра **Доступ к источникам данных за пределами домена** установлено значение **Включить**, то пользователи не будут получать запрос на разрешение междоменного доступа, указанный в таблице. 
  
## <a name="common-language-runtime-code-access-security-features"></a>Функции безопасности для доступа к коду в среде CLR

При компиляции шаблона формы InfoPath с управляемым кодом создается частная сборка с управляемым кодом, в которой содержится реализация логики кода формы.
  
На платформе .NET Framework сборка управляемого кода по умолчанию получает разрешения "Полное доверие" для запуска на локальном компьютере и не получает разрешений "Полное доверие" для запуска в интрасети. Чтобы обеспечить более точный контроль над политикой безопасности и предоставить возможность запуска шаблонов форм InfoPath с управляемым кодом как полностью доверенных форм из интрасети, приложение InfoPath внедряет следующую архитектуру безопасности.
  
- Приложение InfoPath использует среду CLR для платформы .NET Framework.
    
- В используемой InfoPath среде CLR каждый шаблон формы с управляемым кодом запускается на отдельном домене приложения, который представляет собой среду, обеспечивающую границы изоляции, выгрузки и безопасности для исполнения управляемого кода.
    
- Приложение InfoPath устанавливает на домене приложения политику безопасности по умолчанию в зависимости от уровня надежности, связанного с шаблоном формы и URL-адресом его расположения.
    
- По умолчанию шаблон формы с управляемым кодом, запускающийся на локальном компьютере (группа кода зоны "Мой компьютер"), получает разрешения ниже уровня "Полное доверие" (разрешения зоны "Местная интрасеть"). Для получения разрешений "Полного доверие" форму необходимо зарегистрировать или подписать цифровой подписью с доверенного сертификата.
    
Набор политик безопасности, используемый по умолчанию на домене приложения для шаблона формы с управляемым кодом, обеспечивает применение уровней безопасности для доступа к доменам InfoPath, а также любых дополнительных ограничений безопасности .NET. Чтобы обеспечить дополнительную гибкость, система безопасности InfoPath опознает группу кода безопасности "Шаблоны форм InfoPath" для доступа к коду .NET. Если эта группа кода присутствует на компьютере пользователя, то конфигурация безопасности и все возможные дочерние группы кода в рамках этой конфигурации будут применены к домену приложения.
  
> [!IMPORTANT] 
> - Группа кода "Шаблоны форм InfoPath" применяется только непосредственно к сборке кода формы с управляемым кодом. Соответственно, если предоставить набор разрешений "Полное доверие" для кода формы InfoPath с управляемым кодом без установки и регистрации (или цифровой подписи) самого шаблона формы (что обеспечивает полное доверие для всего шаблона формы), то вызовы элементов объектной модели с уровнем безопасности 3 будут по-прежнему выдавать ошибки в коде формы.   
> - Если используется ссылка или явная загрузка (Assembly.Load) сборки, настроенная с помощью ограниченного набора разрешений и использующая свидетельство хэша, строгого имени или издателя для определения условия членства сборки в проекте шаблона формы, то сборка, тем не менее, будет загружена и выполнена шаблоном формы.
    
Сведения о создании и настройке группы шаблонов форм InfoPath см. в тексте Configure Security Параметры шаблонов форм [с кодом.](how-to-configure-security-settings-for-form-templates-with-code.md)
  
В следующей таблице приведены обобщенные сведения о скриптах развертывания и наборах разрешений, применяемых к шаблонам форм с управляемым кодом.
  
|**Сценарий развертывания**|**Набор разрешений**|**Примечания**|
|:-----|:-----|:-----|
|Шаблон форм публикуется на локальном компьютере, а разработчик использует Visual Studio для написания и отладки кода формы.  <br/> |Набор разрешений "Местная интрасеть".  <br/> Сборки, установленные в глобальном кэше сборок (GAC) и отмеченные атрибутом **AllowPartiallyTrustedCallersAttribute**, получают набор разрешений "Полное доверие".  <br/> |По умолчанию шаблоны форм, запускаемые с локального компьютера, не получают набор разрешений "Полное доверие". Разрабатывая шаблоны форм, которые используют функции и вызовы для участников объектной модели, которые требуют разрешений полного доверия, можно использовать процедуру, описанную в шаблонах Предварительного просмотра и Отлаговка форм, которые требуют полного [доверия.](how-to-preview-and-debug-form-templates-that-require-full-trust.md)  <br/> |
|Шаблон формы публикуется на локальном компьютере и указывает ссылку на пользовательскую сборку, которой на этом локальном компьютере требуется набор разрешений "Полное доверие".  <br/> |Набор разрешений "Местная интрасеть".  <br/> Сборки, установленные в глобальном кэше сборок (GAC) и отмеченные атрибутом **AllowPartiallyTrustedCallersAttribute**, получают набор разрешений "Полное доверие". Пользовательская сборка получает набор разрешений "Местная интрасеть".<br/> |Чтобы указать внешние сборки для использования в коде шаблона формы, разработчику необходимо воспользоваться группой кода "Шаблоны форм InfoPath" для предоставления разрешений "Полное доверие" (или соответствующего набора разрешений) для внешней сборки, указанной в коде шаблона формы. Приложение InfoPath не применяет никаких исходных условий для внешних сборок, отличных от установленных в глобальном кэше сборок (GAC). Разработчик должен явным образом предоставить сборке необходимые разрешения с помощью группы кода "Шаблоны форм InfoPath", даже если сборка уже является доверенной благодаря разрешениям, предоставленным в группе кода "My_Computer_Zone".  <br/> |
|Шаблон формы публикуется в общем расположении местной интрасети, например в файловом хранилище, в библиотеке форм SharePoint или на веб-сервере.  <br/> |Набор разрешений "Местная интрасеть".  <br/> Сборки, установленные в глобальном кэше сборок (GAC) и отмеченные атрибутом **AllowPartiallyTrustedCallersAttribute**, получают набор разрешений "Полное доверие".  <br/> ||
|Шаблон формы публикуется в общей папке местной интрасети, например в файловом хранилище, в библиотеке форм SharePoint или на веб-сервере, обозначенном как надежный узел в Internet Explorer.  <br/> |Набор разрешений "Интернет".  <br/> Сборки, подписанные Майкрософт и ECMA, получают набор разрешений "Полный доступ".  <br/> |Безопасность доступа к коду CLR обеспечивает только набор разрешений "Интернет" к сайтам, обозначенным как надежные в Internet Explorer. Приложение InfoPath соблюдает эту политику. Обратите внимание, что данная схема отличается от схемы для шаблонов форм InfoPath, использующих скрипт для кода формы, где при публикации в зоне "Надежные узлы" предоставляется более высокий уровень разрешений.   <br/> |
|Шаблон формы загружается или копируется с веб-сайта.  <br/> |По умолчанию нет. Сборка управляемого кода для шаблона формы не загружается и не запускается.  <br/> ||
   
## <a name="see-also"></a>См. также

- [Настройка безопасности Параметры шаблонов форм с помощью кода](how-to-configure-security-settings-for-form-templates-with-code.md)
- [Шаблоны предварительного просмотра и отлаговки форм, которые требуют полного доверия](how-to-preview-and-debug-form-templates-that-require-full-trust.md)

