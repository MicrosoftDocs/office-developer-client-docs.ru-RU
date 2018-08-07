---
title: IAddrBookDetails
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.Details
api_type:
- COM
ms.assetid: 4eee4382-98c3-4714-8920-8d72edef00b8
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: fbe7f02555f76532896c951f50648c528c250a58
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808767"
---
# <a name="iaddrbookdetails"></a>IAddrBook::Details

  
  
**Относится к**: Outlook 
  
Отображает диалоговое окно, которое предоставляет подробные сведения о записи определенного адресной книги.
  
```cpp
HRESULT Details(
  ULONG_PTR FAR * lpulUIParam,
  LPFNDISMISS lpfnDismiss,
  LPVOID lpvDismissContext,
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  LPFNBUTTON lpfButtonCallback,
  LPVOID lpvButtonContext,
  LPSTR lpszButtonText,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Параметры

 _lpulUIParam_
  
> [in] Указатель на дескриптор родительского окна для диалогового окна.
    
 _lpfnDismiss_
  
> [in] Указатель на функцию, на основе [DISMISSMODELESS](dismissmodeless.md) прототип, или значение NULL. Этот член применим только к безрежимным версии диалоговом окне, указанной флагом DIALOG_SDI задаваемая. MAPI вызывает **DISMISSMODELESS** функцию, если пользователь не закрывает диалоговом окне безрежимным адреса клиента, который вызывает диалоговое окно не является активной **Подробные сведения** о том. 
    
 _lpvDismissContext_
  
> [in] Указатель на сведения о контексте для передачи **DISMISSMODELESS** функции, с помощью параметра _lpfnDismiss_ . Этот параметр применяется только к безрежимным версии диалоговом окне, включая флаг DIALOG_SDI с помощью параметра _ulFlags_ . 
    
 _cbEntryID_
  
> [in] Число байтов в идентификатор записи, на который указывает параметр _lpEntryID_ . 
    
 _lpEntryID_
  
> [in] Указатель на идентификатор записи для входа, для которого отображаются подробные сведения.
    
 _lpfButtonCallback_
  
> [in] Указатель на функцию на основании прототипа функции [LPFNBUTTON](lpfnbutton.md) . В функции **LPFNBUTTON** добавляется кнопка в диалоговом окне "Подробности". 
    
 _lpvButtonContext_
  
> [in] Указатель на данные, используемый в качестве параметра для функции, указанного с помощью параметра _lpfButtonCallback_ . 
    
 _lpszButtonText_
  
> [in] Указатель на строку, которая содержит текст, который применяется для кнопки добавлены, если эта кнопка является расширяемым. Параметр _lpszButtonText_ должен иметь значение NULL, если нет необходимости расширяемая кнопка. 
    
 _ulFlags_
  
> [in] Битовая маска флаги, определяющее тип текста для параметра _lpszButtonText_ . Можно задать следующие флажки: 
    
AB_TELL_DETAILS_CHANGE
  
> Указывает, что **сведения о** возвращает значение S_OK при внесении фактически изменений на адрес; в противном случае **сведения о** возвращает S_FALSE. 
    
DIALOG_MODAL
  
> Отображение модального версии общие адреса диалогового окна, которая всегда находится в отличные от Outlook. Этот флаг является взаимоисключающим с DIALOG_SDI.
    
DIALOG_SDI
  
>  Отображение безрежимным версии стандартным диалоговым окном адрес. Этот флаг игнорируется для клиентов, не являющиеся Outlook. 
    
MAPI_UNICODE 
  
> Строки переданное хранятся в формате Юникод. Если флаг MAPI_UNICODE не установлен, они в формате ANSI.
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> Для записи адресной книги был успешно отображается диалоговое окно "Подробности".
    
## <a name="remarks"></a>Замечания

Клиентские приложения вызовите метод **сведений** для отображения диалогового окна, который предоставляет подробные сведения о конкретной записи в адресной книге. Чтобы добавить кнопку определенного клиента в диалоговое окно, можно использовать параметры _lpfButtonCallback_, _lpvButtonContext_и _lpszButtonText_ . При нажатии кнопки MAPI вызывает функцию обратного вызова, на который указывает _lpfButtonCallback_, передав запись идентификатора кнопки и данные в _lpvButtonContext_. Если вам не требуется расширяемая кнопка, _lpszButtonText_ должен иметь значение NULL. 
  
 **Сведения о** поддерживает Юникод строк символов; Строки Юникод преобразуются в формат многобайтовой строки (MBCS), прежде чем они будут отображаться в диалоговом окне сведения о. 
  
## <a name="mfcmapi-reference"></a>Справочник по mfcmapi (en)

������ ���� mfcmapi (en) ���������� � ������� ����.
  
|**����**|**�������**|**�����������**|
|:-----|:-----|:-----|
|BaseDialog.cpp  <br/> |CBaseDialog::OnOpenEntryID  <br/> |Mfcmapi (en) использует метод **сведений** для отображения диалогового окна, который показывает сведения для записи адресной книги.  <br/> |
   
## <a name="see-also"></a>См. также



[ADRPARM](adrparm.md)
  
[IAddrBook::Address](iaddrbook-address.md)
  
[LPFNBUTTON](lpfnbutton.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

