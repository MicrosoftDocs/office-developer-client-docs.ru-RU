---
title: IMAPIFormContainerResolveMultipleMessageClasses
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormContainer.ResolveMultipleMessageCla
api_type:
- COM
ms.assetid: f18c2dd1-366f-48b4-b335-ebbc0651f467
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 0730da9c3877985853e2cd0a55420e64fbd98e0c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412543"
---
# <a name="imapiformcontainerresolvemultiplemessageclasses"></a>IMAPIFormContainer::ResolveMultipleMessageClasses

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Устраняет группу классов сообщений в их формах в контейнере форм и возвращает массив информационных объектов форм для этих форм.
  
```cpp
HRESULT ResolveMultipleMessageClasses(
  LPSMESSAGECLASSARRAY pMsgClassArray,
  ULONG ulFlags,
  LPSMAPIFORMINFOARRAY FAR * ppfrminfoarray
);
```

## <a name="parameters"></a>Parameters

 _pMsgClassArray_
  
> [in] Указатель на массив, содержащий имена классов сообщений для решения. Имена классов сообщений всегда являются строками ANSI, а не Unicode.
    
 _ulFlags_
  
> [in] Немного флагов, которые контролируют решение классов сообщений. Можно установить следующий флаг:
    
MAPIFORM_EXACTMATCH 
  
> Разрешены только строки класса сообщений, которые соответствуют точному типу.
    
 _ppfrminfoarray_
  
> [вышел] Указатель на указатель на массив информационных объектов форм. Если клиентская заявка передает NULL в  _параметре pMsgClassArray,_ параметр  _ppfrminfoarray_ содержит объекты формы для всех форм в контейнере. 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
## <a name="remarks"></a>Примечания

Клиентские приложения называют **метод IMAPIFormContainer::ResolveMultipleMessageClasses,** чтобы разрешить группу классов сообщений для форм в контейнере форм. Массив объектов информации о форме, возвращаемого в  _параметре ppfrminfoarray,_ предоставляет дополнительный доступ к свойствам каждой формы. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Чтобы разрешить группу классов сообщений формам, передай массив имен классов сообщений, которые необходимо разрешить. Чтобы заставить разрешение быть точным (то есть для предотвращения разрешения для базового класса класса сообщений), флаг MAPIFORM_EXACTMATCH может быть передан в _параметре ulFlags._ 
  
Если класс сообщений не удается разрешить в форму, NULL возвращается для этого класса сообщений в массиве сведений о форме. Поэтому даже если метод возвращает S_OK, не следует предполагать, что все классы сообщений успешно решены. Вместо этого проверьте значения возвращаемого массива.
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|FormContainerDlg.cpp  <br/> |CFormContainerDlg::OnResolveMultipleMessageClasses  <br/> |MFCMAPI использует **метод IMAPIFormContainer::ResolveMultipleMessageClasses,** чтобы найти форму, связанную с набором классов сообщений.  <br/> |
   
## <a name="see-also"></a>См. также



[IMAPIFormContainer::ResolveMessageClass](imapiformcontainer-resolvemessageclass.md)
  
[IMAPIFormContainer : IUnknown](imapiformcontaineriunknown.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

