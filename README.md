<style>

/* ORDER BOX – SMALLER */
.order-box {
  background: var(--card);
  padding: 16px;                  /* reduced */
  border-radius: 14px;
  margin: 30px auto;              /* reduced */
  max-width: 600px;               /* reduced */
  box-shadow: 0 8px 20px rgba(0,0,0,.10);
  border: 1px solid rgba(120,150,120,0.3);
}

/* CONTACT BOX – SMALLER */
.contact-box {
  margin-top: 35px;               /* reduced */
  padding: 18px;                  /* reduced */
  border-radius: 14px;
  background: var(--card);
  box-shadow: 0 8px 18px rgba(0,0,0,.10);
  border-left: 4px solid var(--gold);
  border-right: 4px solid var(--gold);
  font-size: 17px;                /* slightly smaller */
  line-height: 1.7;
}

/* PREMIUM GREEN BACKGROUND ANIMATION */
body::before {
  content: "";
  position: fixed;
  inset: 0;
  background: linear-gradient(
     130deg,
     rgba(180,220,180,0.28),
     rgba(110,160,110,0.32),
     rgba(200,255,200,0.28)
  );
  animation: premiumGreen 10s infinite alternate ease-in-out;
  z-index: -2;
}

@keyframes premiumGreen {
  0% { filter: blur(45px); opacity: .55; }
  100% { filter: blur(75px); opacity: .85; }
}

</style>
