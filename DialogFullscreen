public static void showCcCoinResetPopup(Context ct, String mess) {

        final Dialog dialog = new Dialog(ct);
        dialog.requestWindowFeature(Window.FEATURE_NO_TITLE);
        dialog.getWindow().setFlags(WindowManager.LayoutParams.FLAG_FULLSCREEN, WindowManager.LayoutParams.FLAG_FULLSCREEN);
        dialog.setContentView(R.layout.cc_coin_reset);
        dialog.getWindow().setBackgroundDrawable(new ColorDrawable(Color.TRANSPARENT));
        dialog.getWindow().setLayout(WindowManager.LayoutParams.MATCH_PARENT, WindowManager.LayoutParams.MATCH_PARENT);
        dialog.getWindow().setGravity(Gravity.TOP|Gravity.CENTER_HORIZONTAL);

        TextView txtTitleResetCoin = (TextView) dialog.findViewById(R.id.txtTitleResetCoin);
        TextView txtMessResetCoin = (TextView) dialog.findViewById(R.id.txtMessResetCoin);
        Button btnOK = (Button) dialog.findViewById(R.id.btnOK);

        cUtils.setFont(ct, (ViewGroup) ((ViewGroup)dialog.findViewById(android.R.id.content)).getChildAt(0));

        if (mess == null || mess.equals("")) 
        {
            mess = Utils.getContext().getString(R.string.HACKER_REDEEM);
        }

        txtMessResetCoin.setText(mess);

        dialog.setOnKeyListener(new DialogInterface.OnKeyListener() {
            @Override
            public boolean onKey(DialogInterface dialogInterface, int i, KeyEvent keyEvent) {
                if(keyEvent.getKeyCode() == KeyEvent.KEYCODE_BACK)
                {
                    Toast mToast = Toast.makeText(Utils.getContext(), Utils.getContext().getString(R.string.goback), Toast.LENGTH_LONG);
                    mToast.show();
                }
                return false;
            }
        });

        btnOK.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                dialog.dismiss();
                PopupManager.getInstance().checkShowQueuePopup();
            }
        });

        dialog.setCanceledOnTouchOutside(false);
        dialog.setCancelable(false);
        dialog.show();

    }
